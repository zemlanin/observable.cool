# observable.cool

## examples

- [.take()](http://observable.cool/?black=gray%24.take(3))
- [.skip()](http://observable.cool/?black=gray%24.skip(3))
- [.map()](http://observable.cool/?black=gray%24.map(function(v%2Ci)%7B%20return%20v%5B0%5D%20%7D)&red=gray%24.map(function(v%2Ci)%7B%20return%20i%20%7D))
- [.filter()](http://observable.cool/?black=gray%24.filter(function(v%2Ci)%7B%20return%20v%20%3D%3D%20'ok'%20%7D)&red=gray%24.filter(function(v%2Ci)%7B%20return%20(i%20%25%204)%20%3D%3D%200%20%7D))
- [.filter().map()](http://observable.cool/?black=gray%24.filter(function(v%2Ci)%7B%20return%20v%20%3D%3D%20'ok'%20%7D)&red=black%24.map(function()%7B%20return%20'fine'%20%7D))
- [.pluck()](http://observable.cool/?black=gray%24.timeInterval()&blue=black%24.pluck('interval')&green=black%24.pluck('value'))
- [Rx.Observable.timer()](http://observable.cool/?black=Rx.Observable.timer(0%2C%201000))
- [.pausable()](http://observable.cool/?black=gray%24.map(function%20(v)%20%7B%20return%20v%20%3D%3D%20'up'%20%7D)&red=Rx.Observable.timer(0%2C%201000)&blue=red%24.pausable(black%24))
- [.takeUntil() / .skipUntil()] // TODO
- [.takeWhile() / .skipWhile()] // TODO
- [.startWith()](http://observable.cool/?black=gray%24.map(function%20(v)%20%7B%20return%20v%20%3D%3D%20'up'%20%7D)&red=Rx.Observable.timer(0%2C%201000)&blue=red%24.pausable(black%24)&green=red%24.pausable(black%24.startWith(true)))
- [.share()](http://observable.cool/?black=gray%24.map(function%20(v)%20%7B%20return%20v%20%3D%3D%20'up'%20%7D)&red=Rx.Observable.timer(0%2C%201000).take(10)&blue=red%24.share()&green=red%24.pausable(black%24)&purple=blue%24.pausable(black%24))
- [.scan()](http://observable.cool/?black=gray%24.pluck('length')&red=black%24.scan(function(acc%2C%20v)%7Breturn%20acc%2Bv%7D%2C%200))
- [.reduce()](http://observable.cool/?black=gray%24.pluck('length').take(6)&red=black%24.reduce(function(acc%2C%20v)%7Breturn%20acc%2Bv%7D%2C%200))
- [.sum()](http://observable.cool/?black=gray%24.pluck('length').take(6)&red=black%24.sum())
- [.count()](http://observable.cool/?black=gray%24.take(6)&red=black%24.count())
- [.withLatestFrom() / .combineLatest()](http://observable.cool/?black=gray%24.map(function(v%2C%20i)%7Breturn%20i%7D)&red=Rx.Observable.timer(0%2C%201000)&green=red%24.withLatestFrom(black%24%2C%20Math.max)&purple=red%24.combineLatest(black%24%2C%20Math.max))
- [.flatMap()](http://observable.cool/?black=gray%24.flatMap(function(v)%7Breturn%20Rx.Observable.timer(500%2C%201500).take(3)%20%7D))
- [.switch()](http://observable.cool/?black=gray%24.map(function(v)%7Breturn%20Rx.Observable.timer(0%2C%201000).map(v)%7D)&blue=black%24.switch())
