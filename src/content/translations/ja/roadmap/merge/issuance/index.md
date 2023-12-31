---
title: マージがETHの供給に与えた影響について
description: マージがETHの供給に与えた影響についての概要
lang: ja
---

# マージが ETH の供給に与えた影響について {#how-the-merge-impacts-ETH-supply}

マージとは、2022 年 9 月にイーサリアムネットワークがプルーフ・オブ・ワークからプルーフ・オブ・ステークへ移行したアップデートのことです。 この移行により、ETH の発行方法が変更されました。 以前は、実行レイヤー( メインネット)とコンセンサスレイヤー( ビーコンチェーン)の 2 つのレイヤーから発行されていましたが、 マージ以降は、実行レイヤーで発行されなくなりました。 それでは、詳しく見ていきましょう。

## ETH を発行するコンポーネント {#components-of-eth-issuance}

ETH の供給は、「発行」と「バーン」という 2 つの主要な要因に分けられます。

ETH の**発行**は、ETH を作成するプロセスで以前は存在しなかった仕組みです。 ETH を破壊して流通から排除することを**バーン**といいます。 発行とバーンの割合は、いくつかのパラメータに基づいて計算されます。発行とバーンのバランスによって、イーサのインフレ/デフレ率が決まります。

<Card
emoji=":chart_decreasing:"
title="ETHの発行についての概要">

- プルーフ・オブ・ステークに移行する前、マイナー全体で、1 日あたり約 13,000ETH を発行していました。
- ステーキングされている計約 1,400 万 ETH に基づいて、1 日あたり約 1,700ETH がステーカーに発行されます。
- ステーキングによる正確な発行量は、ステーキングされた ETH の総量に応じて変動します。
- **マージ以降、1 日あたり最大 1,700ETH しか発行されなくなり、新たな ETH の発行総量は、最大で約 88%減少しています**
- バーンは、ネットワークの需要に応じて変動します。 とある日に、平均のガス価格が 16Gwei 以上になると、バリデータによって発行される約 1,700ETH が実質的に相殺されるので、その日の純 ETH インフレ率はゼロ以下になります。

</Card>

## マージ以前(過去) {#pre-merge}

### 実行レイヤーでの発行 {#el-issuance-pre-merge}

プルーフ・オブ・ワークでは、マイナーは実行レイヤーのみとやり取りを行い、最初に次のブロックを解決したマイナーがブロック報酬を受け取っていました。 2019 年の[コンスタンティノープルアップグレード](/history/#constantinople)以降、ブロックごとの報酬は 2ETH になりました。 マイナーは、[オマー](/glossary/#ommer)ブロック(最長または正規チェーンに含まれない有効なブロック)を発行しても報酬を受けました。 オマーブロックあたりの報酬は最大 1.75 ETH で、正規ブロックから発行された報酬とは*別*でした。 マイニングのプロセスは経済的に集中化された活動であり、これを維持するには、ETH の発行量を歴史的に高い水準に維持する必要があったのです。

### コンセンサスレイヤーでの発行 {#cl-issuance-pre-merge}

2020 年に稼働を開始した[ビーコンチェーン](/history/#beacon-chain-genesis)では、 マイナーに代わって、バリデータがプルーフ・オブ・ステークでネットワークを保護します。 ビーコンチェーンは、イーサリアムユーザーがメインネット(実行レイヤー)上のスマートコントラクトに ETH を一方向に入金することによってブートされます。ビーコンチェーンは、この入金をリッスンしており、ユーザーに対して新しいチェーンに同額の ETH をクレジットします。 マージが起こるまで、ビーコンチェーンのバリデータは、トランザクションの処理を行わず、基本的にはバリデータプールの状態についてのコンセンサスを形成していました。

ビーコンチェーンのバリデータは、チェーンの状態を証明し、ブロックを提案することで、報酬として ETH を受け取ります。 報酬(またはペナルティ)は、バリデータのパフォーマンスに応じて、各エポック(6.4 分ごと)に計算、分配されます。 バリデータの報酬は、プルーフ・オブ・ワーク時代のマイニング報酬(約 13.5 秒ごとに 2ETH)と比べて**大幅**に少なくなっています。これは、バリデータノードの運用にそれほどコストがかからないため、高い報酬は必要ないからです。

### マージ以前の発行についての概要 {#pre-merge-issuance-breakdown}

総 ETH 供給量: **約 120,520,000ETH**(2022 年 9 月のマージ時点)

**実行レイヤーでの発行**

- 13.3 秒あたり 2.08ETH と推定されています。\*: 年間で**約 4,930,000**ETH が発行される計算になります。
- 結果、**約 4.09%**のインフレ率(年間 493 万/合計 1 億 2050 万)。
- \*この計算には、正規ブロックごとに発行される 2ETH と、その期間におけるオマーブロックの平均 0.08ETH が含まれています。 また、[ディフィカルティボム](/glossary/#difficulty-bomb)の影響を受けないベースラインブロック時間ターゲットである 13.3 秒を使用しています。 ([参照元をご覧ください](https://bitinfocharts.com/ethereum/))

**コンセンサスレイヤーでの発行**

- ステーキングされた合計が 14,000,000ETH だと、ETH 発行レートは、1 日あたり約 1700ETH になります。([参照元をご覧ください](https://ultrasound.money/))
- 年間で**約 620,500**ETH が発行される計算になります。
- 結果、**約 0.52%**のインフレ率(年間 62 万 500/合計 1 憶 1930 万)。

<InfoBanner>
<strong>合計年発行率(マージ前): 約4.61%</strong> (4.09% + 0.52%)<br/><br/>
発行額の<strong>約 88.7%</strong>が実行レイヤー (4.09 / 4.61 * 100) のマイナーへ帰属しました。<br/><br/>
<strong>約11.3%</strong>がコンセンサスレイヤーのステーカーへ発行されました (0.52 / 4.61 * 100) 。
</InfoBanner>

## マージ以降(現在) {#post-merge}

### 実行レイヤーでの発行 {#el-issuance-post-merge}

マージ以降、実行レイヤーでの発行は行われなくなりました。 マージによってアップグレードされたコンセンサスルールでは、プルーフ・オブ・ワークはブロック生成に使用できなくなりました。 実行レイヤーのすべてのアクティビティは、「ビーコンブロック」にまとめられ、プルーフ・オブ・ステークにおけるバリデータによって公開、証明されるようになりました。 ビーコンブロックの証明・公開に対する報酬は、コンセンサスレイヤーで個別に計算されます。

### コンセンサスレイヤーでの発行 {#cl-issuance-post-merge}

コンセンサスレイヤーでの発行は、マージ以前から同様に現在も続いており、ブロックを証明して提案したバリデータには少額の報酬が支払われます。 報酬は、コンセンサスレイヤー内で管理される*バリデータ残高*に積み立てられ、 メインネット上でトランザクションが可能な現行のアカウント (「実行」アカウント)とは別のイーサリアムアカウントに蓄積されます。そのため、他のイーサリアムアカウントとの自由なトランザクションはできません。 また、これらのアカウントの資金は、指定された 1 つの実行アドレス以外には引き出すことができません。

2023 年 4 月に実施された上海/カペラのアップグレードにより、ステーカーは引き出しが可能になりました。 ただし、*収益/報酬(32ETH を越える残高)*は、ステークウェイト(最大 32)として貢献しないため、引き出さない方がよいとされています。

ステーカーは、バリデータの残高すべてを引き出して、アクティビティを終了することもできます。 ただし、イーサリアムの安定性を確保するために、同時に終了するバリデータの数には上限が設けられています。

1 日あたち、すべてのバリデータのうち約 0.33%が終了できます。 デフォルトでは、エポックごとに 4 台のバリデータが終了できます(6.4 分ごと 4 台、1 日では 900 台) 。 バリデータ数が 262,144(2<sup>18</sup>)台を超えると、65,536(2<sup>16</sup>)台のバリデータが増設されるたびに、追加で 1 台のバリデータが終了できます。 例えば、バリデータが 327,680 台を超えると、エポックごとに 5 台が終了すします(1 日あたり 1,125 台) 。 アクティブなバリデータ数が 393,216 台を超えると、6 台の終了が許可されます(以降も同様です)。

多数のバリデータが引き出すと、ネットワークが不安定になる可能性があるため、終了するバリデータの最大数を 4 台に縮小し、「ステーキングされた ETH が一度に大量に引き出されること」を防ぎます。

### マージ以降のインフレについての概要 {#post-merge-inflation-breakdown}

- 総 ETH 供給量: **約 120,520,000ETH**(2022 年 9 月のマージ時点)
- 実行レイヤーでの発行: **0**(なし)
- コンセンサスレイヤーでの発行: 上記(マージ以前)と同じで、年間発行率**約 0.52%**(合計 1,400 万 ETH がステーキングされている場合)

<InfoBanner>
合計年間発行率: <strong>約0.52%</strong><br/><br/>
年間ETH発行の純削減率: <strong>約88.7%</strong> ((4.61% - 0.52%) / 4.61% * 100)
</InfoBanner>

## <Emoji text=":fire:" size="1" />バーン(焼却) {#the-burn}

ETH の発行とは逆に、イーサリアムでは ETH がバーンされるレートがあります。 イーサリアムでトランザクションを実行するには、最低手数料(「ベースフィー」)を支払う必要があります。ベースフィーは、ネットワークの混雑状況によって(ブロックごとに)常に変動し、 ETH で支払われます。ベースフィーは、トランザクションが有効に成立するために*必要*となり、 トランザクション処理中に*バーン*され、流通から消滅します。

<InfoBanner>
フィーのバーンは、2021年8月の<a href="/history/#london">ロンドンアップグレード</a>から始まり、マージ以降も継続されます。
</InfoBanner>

ロンドンのアップグレードで実装されたフィーのバーンに加えて、バリデータがオフラインになるとペナルティを課されます。さらに深刻なことに、ネットワークのセキュリティを脅かす特定のルールに違反した場合にはスラッシュされることがあります。 これらのペナルティにより、バリデータの残高から ETH が減少し、他のどのアカウントにも直接報酬として支払われず、事実上は流通から消滅することになります。

### デフレ時における平均ガス価格の計算 {#calculating-average-gas-price-for-deflation}

上述したように、特定の日に発行される ETH の量はステーキングされた ETH の合計額によって決まります。 この記事の執筆時点では、1 日あたり約 1700ETH が発行されています。

指定された 24 時間内で、ETH の発行を完全に相殺するのに必要な平均ガス価格を決定するには、ブロック時間を 12 秒として、1 日の総ブロック数を計算することから始めます。

- `(1ブロック/12秒) * (60秒/分) = 5ブロック/分`
- `(5ブロック/分) * (60分/時間) = 300ブロック/時間`
- `(300ブロック/時間) * (24時間/日) = 7200ブロック/日`

各ブロックは、`15x10^6 gas/block`をターゲットとしています([ガスの詳細](/developers/docs/gas/))。 1 日あたりの合計 ETH 発行量が 1700ETH であるとすると、発行を相殺するために必要な平均ガス価格(ガスあたりの gwei)は、次の計算式で求めることができます。

- `7200 blocks/day * 15x10^6 gas/block *`**`Y gwei/gas`**`* 1 ETH/ 10^9 gwei = 1700 ETH/day`

`Y`を次のように求めます。

- `Y = (1700(10^9))/(7200 * 15(10^6)) = (17x10^3)/(72 * 15) = 16 gwei`(有効数字 2 桁に丸める)

上記の最終ステップを再構成するもう 1 つの方法は、`1700`を 1 日あたりの ETH 発行量を意味する変数`X`に置き換え、残りは次のように単純化します。

- `Y = (X(10^3)/(7200 * 15)) = X/108`

これは、`X`の関数として単純化することができます。

- `f(X) = X/108`: ここで`X`は、ETH の一日の発行量、そして`f(X)`は、新しく発行されたすべての ETH を相殺するために必要なガス価格あたりの gwei を表しています。

したがって、例えば`X`(一日の ETH 発行量)がステークされた合計 ETH 量をもととして 1800ETH になったとすると、`f(X)`(すべての発行量を相殺するために必要な gwei) は、`17gwei`となります(有効数字 2 桁の場合) 。

## さらに学びたい方へ {#further-reading}

- [マージ](/roadmap/merge/)
- [Ultrasound.money](https://ultrasound.money/) - _ETH の発行とバーンをリアルタイムで可視化したダッシュボードが利用可能_
- [Charting Ethereum Issuance](https://www.attestant.io/posts/charting-ethereum-issuance/) - _Jim McDonald 2020_
