```javascript
 const paramStr = "page=1&size=20";
  const actionUrl = "/export/XXX?" + paramStr;
  const exportForm = document.createElement('form');
  exportForm.style.display = "none";
  exportForm.setAttribute('action', actionUrl);
  exportForm.setAttribute('method', 'post');
  document.body.appendChild(exportForm);
  exportForm.submit();
  
  setTimeout(() => {
    document.body.removeChild(exportForm);
  }, 3000);
```
