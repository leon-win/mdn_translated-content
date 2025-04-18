---
title: プライバシー、権限、情報セキュリティについて
slug: Web/Privacy
l10n:
  sourceCommit: d5881638fe69ade2c24854af16f014291ad758e2
---

{{QuicklinksWithSubPages}}

ユーザーが日常的にウェブを使用するようになると、プライベートな情報や個人を特定する情報を共有することが多くなりますが、できれば信頼できるサイトとだけ共有したいものです。そのため、コンテンツ、ウェブブラウザー、ウェブサーバーが連携して、プライバシーや情報セキュリティの確保に努めることが必要です。この記事では、ユーザーの個人情報や画像が第三者に意図せず取得されるリスクを最小化するウェブコンテンツを作成する方法について検討します。

## セキュリティとプライバシーの定義

ウェブ上でユーザーが利用できるさまざまなセキュリティやプライバシー機能について詳しく説明する前に、いくつかの重要な用語を定義しておきましょう。

- 個人を特定できる情報

  - : 個人を特定できる情報 (Personally identifiable information, PII) とは、その全部または一部を使用して、特定の個人を追跡したり、特定したりすることができる情報のことです。そのため、PII はウェブにとどまらず、生活のすべての場面に及んでいます。例えば、あるサイトがユーザーの名前と郵便番号のリストをオンライン上に流出させた場合、悪い業者は、対応する電話帳を使用することで、そのユーザーの少なくとも何割かを特定できることはほぼ間違いありません。

    個人を特定する情報には、ユーザー名、本名、パスワード、電話番号や住所（あるいはその一部）、病歴に関する情報、社会保障番号、運転免許証、あるいはその他IDやID番号の形成する形式、クレジットカード情報などを含めることができます。とても広い範囲の情報です。データを作業するときは、常に立ち止まって考えてください。多くの手順を経て、ある人物を特定するために使用できる方法はないでしょうか？

- プライバシー

  - : プライバシーの概念を定義するのは、やや困難です。何かを秘密にすることの意味については、誰もが何らかの考えを持っていますが、データのプライバシーについて話すときは、それが不明瞭になります。基本的に、インターネット上のデータのプライバシーとは、個人的な意味を持つ情報を、その入手方法にかかわらず、権限のない人や組織の手に渡らないようにすることを意味します。

    プライバシーの例外は、特定のサイトやアプリケーションに対して認められることもありますが、一部の人だけにアクセスを許可したり、限られた時間だけ情報へのアクセスや使用を許可したりするなど、条件付きで認められることもあります。

- セキュリティ
  - : セキュリティとは、データやシステムを、その権限を持たない人や組織によってアクセスされたり、ダウンロードされたり、運営されたりしないように、積極的に保護することをいいます。優れたセキュリティ対策は、対象とするものが何であれ、システムやデータへの不正なアクセスを防止することを目的としています。

## 個人・プライベート情報

<!--what kind of information is private or personal?-->

## プライバシーリスク

<!--what are ways personal information can be gotten by third parties?-->

### フィンガープリント

**フィンガープリント**は、ユーザーのブラウザーによって利用できるさまざまな情報を収集し、そのユーザーのブラウザーを一意に識別できるようになるまで照合するために使用される技術です。一見無害な情報でも、原理的にはフィンガープリント作業に使用することができますが、特定の機器に固有の情報であればあるほど、より効果的です。

現代のブラウザーは、情報へのアクセスを許可しないか、情報を利用できるようにする必要がある場合は、識別のために使用することを防ぐ様々な方法を導入することによって、フィンガープリントに基づく攻撃を防ぐのに役立つ措置を講じています。

例えば、ウェブサイトがユーザーのブラウザーに経過時間を問い合わせた場合、その時刻とサーバーが報告した時刻を比較することで、フィンガープリントの要因として有益なものとなる可能性があります。このため、ブラウザーは通常、タイマーをユーザーシステムの識別に使用されにくくするために、タイマーに少量の変動を導入しています。

## 新しいプライバシー技術

ウェブブラウザーは、プライバシー空間を改善する新しい機能に積極的に取り組んでいます。

{{ListSubpages()}}

## プライバシーとセキュリティの制御

セキュリティやプライバシーの侵害からユーザーを守るための支援として、複数の制御レイヤーがあります。これらは、ネットワーク上で使用される通信層を含むウェブサーバーから始まり、ウェブブラウザーのセキュリティ機能を経て、ウェブアプリケーションのコードに到達し、それ自身とユーザーが託したデータを保護するために取る努力に至ります。

プライバシーとセキュリティを管理するために、いくつかのウェブ技術や機能があります。以下のリストは、これらの機能の多くが両方に使用されるため、両方に影響を与える機能を記載しています。

<table class="standard-table" style="max-width: 42rem">
  <caption>
    セキュリティとプライバシーを強化するために使用されるウェブ技術と機能
  </caption>
  <thead>
    <tr>
      <th scope="col">技術または機能</th>
      <th scope="col">説明</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <a href="/ja/docs/Web/Security/Certificate_Transparency">資格情報の透明性</a>
      </td>
      <td>
        証明書を監視・監査するためのオープンスタンダードで、不正な証明書や悪意のある証明書の特定に支援するために使用できる公開ログのデータベースを作成します。
      </td>
    </tr>
    <tr>
      <td><a href="/ja/docs/Web/HTTP/Guides/CSP">コンテンツセキュリティポリシー</a></td>
      <td>
        文書内のコンテンツがウェブ上で他の機器からアクセスできる範囲を定義する機能を提供した。特にサーバーへの攻撃を防止または軽減するために使用できる。
      </td>
    </tr>
    <tr>
      <td>
        <a href="/ja/docs/Web/HTTP/Reference/Headers/Strict-Transport-Security">HTTP Strict Transport Security</a> (HSTS)
      </td>
      <td>
        HSTS は、サイトがクライアントに対してサーバーとの通信に HTTPS のみを使用することを指示することによって、プロトコルのダウングレードやクッキーハイジャック攻撃から自身を保護するためにサーバーから使用されます。
      </td>
    </tr>
    <tr>
      <td><a href="/ja/docs/Glossary/HTTP_2">HTTP/2</a></td>
      <td>
        HTTP/2 は技術的には暗号化を使用する必要はありませんが、ほとんどのブラウザー開発者は HTTPS と併用する場合のみ対応しているので、その点でセキュリティに関連していると考えることもできます。
      </td>
    </tr>
    <tr>
      <td><a href="/ja/docs/Web/API/Permissions_API">権限 API</a></td>
      <td>
        現在のブラウザーコンテキストに対する権限の状態を判断する方法を提供します。
      </td>
    </tr>
    <tr>
      <td><a href="/ja/docs/Web/HTTP/Guides/Permissions_Policy">権限ポリシー</a></td>
      <td>
        ウェブサーバーが {{HTMLElement("iframe")}} で読み込んだ文書とサブ文書の両方で、{{HTTPHeader("Permissions-Policy")}} を介して機能や API を選択的に有効または無効にできるようにします。
        <a href="/ja/docs/Web/HTML/Element/iframe#allow"><code>allow</code></a> 属性は、個々の {{HTMLElement("iframe")}} に権限ポリシーを設定するために使用できます。
      </td>
    </tr>
    <tr>
      <td>
        <a href="/ja/docs/Web/Security/Transport_Layer_Security">Transport Layer Security</a>
        (TLS)、以前は Secure Sockets Layer (SSL) と呼ばれていました
      </td>
      <td>
        TLS は、ネットワーク上での転送中にデータを暗号化することで、セキュリティとプライバシーを提供します。これは、<a href="/ja/docs/Glossary/HTTPS">HTTPS</a> (HyperText Transport Protocol Secured) プロトコルを支える技術です。
      </td>
    </tr>
  </tbody>
</table>

## 個人情報の安全管理

## サイトの権限の管理

## すべての統合

<!--using Feature Policy with permissions and so forth; how to use them together, how they interact, etc.-->

### \<iframe> 要素内の権限リクエスト

ウェブアプリケーションが {{HTMLElement("iframe")}} 要素を使用して他のサイトのコンテンツを自分のサイト内に埋め込む場合、特にフレームに読み込む文書にその権限を考える必要がある場合は、厄介なことになることがあります。

これらの技術の仕様は、このような状況を処理するための戦術を表明または推奨していますが、ブラウザーは、セキュリティをさらに向上させたり、新しい機能を試したり、ユーザーにとっての複雑さを軽減したりするために、異なる解決策を提供する可能性があり、他にもさまざまな理由が考えられます。

<!-- allow attribute, feature policy, and permissions api stuff -->

リソースへのアクセスを許可して読み込んだ文書が、{{HTMLElement("iframe")}} の中に [`allow`](/ja/docs/Web/HTML/Reference/Elements/iframe#allow) 属性を含んでいて、その許可をフレームのコンテンツに委任している場合、使い勝手の問題が生じることがあります。この場合、ユーザーは同じリソースを繰り返しリクエストされることになり、最初はメインページ、次にフレーム内の文書でリクエストされる可能性があります。

ブラウザーは、これを回避する方法を提供することができます。例えば、Firefox 73 では、ユーザー権限リクエストが修正され、`<iframe>` が `allow` キーワードを使用して埋め込み文書に権限を委譲する場合、ブラウザーは親文書にリソースを使用する権限を与えるようユーザーに要求し、その権限はリソースをリクエストした埋め込みコンテンツと共有され、始めに使用します。

<!-- diagram and/or code snippet to clarify things-->

## 関連情報

- [ウェブセキュリティ](/ja/docs/Web/Security)
- [権限 API](/ja/docs/Web/API/Permissions_API)
- [権限ポリシー](/ja/docs/Web/HTTP/Guides/Permissions_Policy)
- [The Privacy Sandbox](https://developer.google.com/privacy-sandbox)
