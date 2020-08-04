# 1. 要件
* 必ず読む。
* 必要な条件を見極める。ストレージはくどい説明を行っていないSASを選択する。

## ESXi 7.0の要件を見てみる
<a href="https://docs.vmware.com/jp/VMware-vSphere/7.0/com.vmware.esxi.upgrade.doc/GUID-DEB8086A-306B-4239-BF76-E354679202FC.html" target="_blank">ESXiのハードウェア要件(esxi7.0)</a>

### 要件抜粋
1. <a href="https://www.vmware.com/resources/compatibility/search.php" target="_blank">VMware Compatibility Guide</a>
2. CPUは2コア以上
3. メモリは8G以上
4. ストレージはインストール領域だけで142GB以上
5. vSphereの場合はVCSA分も確保すること

### 1. VMware Compatibility Guide
<a href="https://www.vmware.com/resources/compatibility/search.php" target="_blank">リンク</a>

例としてDell R6515を指定して検索すると7.0, 6.7u3, 6.5u3にヒットする
* 検索ヒットすれば、CPUのIntel VT/AMD RViやNX/XDビットなどの細かなハードウェア仕様はクリアできている
* 検索ヒットしない場合は動作に支障があるということ。他のハードウェアを選定すべき

### 2. CPUは2コア以上
* 2ソケットや2スレッドではない
* ゲストOS要件で最低クロック数を指定している場合がある

### 3. メモリは8G以上
* ハイパーバイザー分だけで8GB確保すること
* ゲストOSの必要メモリを積み上げること
* メモリ共有機能に期待しないこと

### 4. ストレージはインストール領域だけで142GB以上
* くどい説明を行っていないSASを選択する

### 5. vSphereの場合はVCSA分も確保すること
<a href="https://docs.vmware.com/jp/VMware-vSphere/7.0/com.vmware.vcenter.upgrade.doc/GUID-752FCA83-1A9B-499E-9C65-D5625351C0B5.html" target="_blank">vCenter Serverアプライアンスのシステム要件</a>

## RedHat KVMの要件を見てみる
<a href="https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/virtualization_deployment_and_administration_guide/sect-system_requirements-kvm_requirements" target="_blank">KVM Hypervisor Requirements</a>

### 要件抜粋
* Intel VT/AMD RVi対応のみ

実際にはESXiと同じ要件で選出

## Hyper-Vの要件を見てみる
<a href="https://docs.microsoft.com/ja-jp/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows" target="_blank">Windows Server状のHyper-Vシステム要件</a>

### 要件抜粋
* 機械翻訳で何言ってるかわからねぇ
* 英語のリンクを読んでも本質的なことが書かれていないのでまたわからねぇ

実際にはESXiと同じ要件で選出  
ただし、物理サーバーへWindows Serverをインストールして使用する場合はWindows Serverの要件分を追加する。  
<a href="https://docs.microsoft.com/ja-jp/windows-server/get-started-19/sys-reqs-19" target="_blank">Winmdows Server 2019 システム要件</a>

