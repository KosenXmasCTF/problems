[Repository](https://github.com/KosenXmasCTF/change_me)

<!-- なにか言いたいことがあれば -->

## Template for Reviewers
```md
### Checklist
<!-- [ ] を [x] にする -->
- [x] 問題は成立しているか？
- [x] エスパー要素はないか？
- [x] つまらない妨害要素はないか？
- [x] ランダム / 総当たり要素は許容範囲か？
- [x] 問題を破壊できる可能性はあるか？
- [x] サーバーに過度な負荷がかからないか？
- [ ] 非想定解は存在しないか？
- [x] 難易度は適正か？

### Writeup
<!-- レビュアーの解法を書く　方針や詰まった点がわかれば良し -->
main関数を見たら、wait,generate_flag,strcmpが使われており、strcmpに直接入力を渡していることから、generate_flagでフラグが生成されたとわかる。
まずwaitをバイパスする。gdbでwaitにブレイクポイントを掛けてジャンプ、generate_flagが終わったらvmmapでそれっぽいところにsearchmem、フラグが得られる。

### Suggestions
<!-- 改善の提案 -->
カウントダウンが終わったら何が起こるのかわかりづらそう。
文字列の比較ができるようになる旨を教えてあげれば、アセンブリも読みやすくなると思う。easyなので

### Memo
<!-- その他，備考 -->
```
