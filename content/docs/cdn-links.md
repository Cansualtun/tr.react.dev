---
id: cdn-links
title: CDN Bağlantıları
permalink: docs/cdn-links.html
prev: create-a-new-react-app.html
next: release-channels.html
---

Hem React'e hem de ReactDOM'a CDN üzerinden ulaşılabilir.

```html
<script crossorigin src="https://unpkg.com/react@16/umd/react.development.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
```

Yukarıdaki sürümler yalnızca geliştirme amaçlıdır ve yayınlamaya uygun değildir. React'in küçültülmüş ve optimize edilmiş yayınlamaya uygun sürümleri şu adreste mevcuttur:

```html
<script crossorigin src="https://unpkg.com/react@16/umd/react.production.min.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@16/umd/react-dom.production.min.js"></script>
```

`react`'in ve `react-dom`'un belirli bir sürümünü yüklemek için, `16`'yı istediğiniz sürüm numarası ile değiştirin.

### Neden `crossorigin` Özelliği? {#why-the-crossorigin-attribute}

Bir CDN'den React kullanıyorsanız, [`crossorigin`](https://developer.mozilla.org/en-US/docs/Web/HTML/CORS_settings_attributes) özelliğini ayarlı tutmanızı öneririz:

```html
<script crossorigin src="..."></script>
```

Ayrıca, kullandığınız CDN’nin `Access-Control-Allow-Origin: *` HTTP başlığını ayarladığını doğrulamanızı öneririz:

![Access-Control-Allow-Origin: *](../images/docs/cdn-cors-header.png)

Bu, React 16 ve sonraki sürümlerinde daha iyi bir [hata yönetme deneyimi](/blog/2017/07/26/error-handling-in-react-16.html) sağlar.
