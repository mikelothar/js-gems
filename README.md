# js-gems

### Sort by multiple columns (jQuery)
Some user elements with an "Is currently online" overlay, sorted alphabetically, but with the online users at the top of the list.
```javascript
userElements.sort(function (a, b) {
  const $a = $DS(a)
  const $b = $DS(b)
  const an = $a.find('.js-user-name')[0].innerText
  const bn = $b.find('.js-user-name')[0].innerText
  const av = $a.find('.js-user-online').is(':visible')
  const bv = $b.find('.js-user-online').is(':visible')
  if (av > bv) return -1
  if (av < bv) return 1
  if (an < bn) return -1
  if (an > bn) return 1
  return 0
})
```
