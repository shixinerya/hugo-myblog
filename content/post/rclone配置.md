# rclone配置



### 配置 Rclone

输入 `rclone config` 命令，会出现以下信息，参照下面的注释进行操作。



<details open="" style="box-sizing: border-box; display: block;"><summary style="box-sizing: border-box; display: list-item; cursor: pointer; outline: 0px;">点击查看</summary><p style="box-sizing: border-box; margin: 0.92em 0px;"></p><blockquote style="box-sizing: border-box; margin: 0.92em 0px; border-width: 4px; border-left-style: solid; border-color: rgba(255, 255, 255, 0.05); padding-left: 12px; color: rgb(170, 170, 170);"><strong style="box-sizing: border-box; font-weight: 700; color: rgb(206, 206, 207);">TIPS:</strong><span>&nbsp;</span>因为 RCLONE 会时不时进行更新，当你看到这篇教程时菜单选项可能已经发生了略微的改动，但大致思路不会变，<strong style="box-sizing: border-box; font-weight: 700; color: rgb(206, 206, 207);">不要无脑照搬操作</strong>。</blockquote><pre class=" language-none line-numbers" style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 0.96em; position: relative; width: 820px; overflow: hidden; line-height: 1.5; border: none; border-radius: 5px; background: rgb(17, 17, 17); text-align: left; white-space: pre; word-spacing: normal; word-break: normal; overflow-wrap: normal; tab-size: 4; hyphens: none; counter-reset: linenumber 0; color: rgb(204, 204, 204);"><code class=" language-none" style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(17, 17, 17); padding: 10px 10px 10px calc(3em + 10px); border-radius: 3px; text-align: left; white-space: inherit; word-spacing: normal; word-break: normal; overflow-wrap: normal; tab-size: 4; hyphens: none; display: block; overflow: auto; color: rgb(204, 204, 204);">e) Edit existing remote
n) New remote
d) Delete remote
r) Rename remote
c) Copy remote
s) Set configuration password
q) Quit config
e/n/d/r/c/s/q&gt; n  # 选择n，新建
name&gt; P3TERX   # 输入名称，类似于标签，用于区分不同的网盘。
Type of storage to configure.
Enter a string value. Press Enter for the default ("").
Choose a number from below, or type in your own value
 1 / A stackable unification remote, which can appear to merge the contents of several remotes
   \ "union"
 2 / Alias for a existing remote
   \ "alias"
 3 / Amazon Drive
   \ "amazon cloud drive"
 4 / Amazon S3 Compliant Storage Providers (AWS, Ceph, Dreamhost, IBM COS, Minio)
   \ "s3"
 5 / Backblaze B2
   \ "b2"
 6 / Box
   \ "box"
 7 / Cache a remote
   \ "cache"
 8 / Dropbox
   \ "dropbox"
 9 / Encrypt/Decrypt a remote
   \ "crypt"
10 / FTP Connection
   \ "ftp"
11 / Google Cloud Storage (this is not Google Drive)
   \ "google cloud storage"
12 / Google Drive
   \ "drive"
13 / Hubic
   \ "hubic"
14 / JottaCloud
   \ "jottacloud"
15 / Local Disk
   \ "local"
16 / Mega
   \ "mega"
17 / Microsoft Azure Blob Storage
   \ "azureblob"
18 / Microsoft OneDrive
   \ "onedrive"
19 / OpenDrive
   \ "opendrive"
20 / Openstack Swift (Rackspace Cloud Files, Memset Memstore, OVH)
   \ "swift"
21 / Pcloud
   \ "pcloud"
22 / QingCloud Object Storage
   \ "qingstor"
23 / SSH/SFTP Connection
   \ "sftp"
24 / Webdav
   \ "webdav"
25 / Yandex Disk
   \ "yandex"
26 / http Connection
   \ "http"
Storage&gt; 18  # 选择18，Microsoft OneDrive
** See help for onedrive backend at: https://rclone.org/onedrive/ **

Microsoft App Client Id
Leave blank normally.
Enter a string value. Press Enter for the default ("").
client_id&gt;   # 留空，回车
Microsoft App Client Secret
Leave blank normally.
Enter a string value. Press Enter for the default ("").
client_secret&gt;   # 留空，回车
Edit advanced config? (y/n)
y) Yes
n) No
y/n&gt; n  # 选n
Remote config
Use auto config?
 * Say Y if not sure
 * Say N if you are working on a remote or headless machine
y) Yes
n) No
y/n&gt; n  # 选n
For this to work, you will need rclone available on a machine that has a web browser available.
Execute the following on your machine:
    rclone authorize "onedrive"
Then paste the result below:
result&gt; {"XXXXXXXX"}  # 上面保存的token复制到这里
2018/10/31 19:54:06 ERROR : Failed to save new token in config file: section 'P3TERX' not found
Choose a number from below, or type in an existing value
 1 / OneDrive Personal or Business
   \ "onedrive"
 2 / Root Sharepoint site
   \ "sharepoint"
 3 / Type in driveID
   \ "driveid"
 4 / Type in SiteID
   \ "siteid"
 5 / Search a Sharepoint site
   \ "search"
Your choice&gt; 1  # 这里问你要选择的类型，选1
Found 1 drives, please select the one you want to use:
0: OneDrive (business)
Chose drive to use:&gt; 0  # 程序找到网盘，这里编号是0，就选择0
Found drive 'root' of type 'business', URL: https://xxxxxx-my.sharepoint.com/personal/xxxxxxx/Documents
Is that okay?
y) Yes
n) No
y/n&gt; y  # 选y
--------------------
[P3TERX]
type = onedrive
token = {"XXXXXXXX"}
drive_id = XXXXXXXXX
drive_type = business
--------------------
y) Yes this is OK
e) Edit this remote
d) Delete this remote
y/e/d&gt; y  # 选y
Current remotes:

Name                 Type
====                 ====
P3TERX               onedrive

e) Edit existing remote
n) New remote
d) Delete remote
r) Rename remote
c) Copy remote
s) Set configuration password
q) Quit config
e/n/d/r/c/s/q&gt; q  # 选q，退出</code><span aria-hidden="true" class="line-numbers-rows" style="box-sizing: border-box; position: absolute; pointer-events: none; top: 10px; font-size: 17.28px; left: 0px; width: 3em; letter-spacing: -1px; border-right: 1px solid rgba(153, 153, 153, 0.2); user-select: none; background: rgb(17, 17, 17);"><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span></span></pre><p style="box-sizing: border-box; margin: 0.92em 0px;">至此，Rclone 已成功连接到了 OneDrive 网盘。</p><p style="box-sizing: border-box; margin: 0.92em 0px;"></p><h2 id="toc_5" style="box-sizing: border-box; font-family: &quot;PingFang SC&quot;, &quot;Hiragino Sans GB&quot;, &quot;Microsoft Yahei&quot;, &quot;WenQuanYi Micro Hei&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;, Helvetica, Arial, -apple-system, system-ui, sans-serif; color: rgb(206, 206, 207); position: relative; font-size: 1.5em; margin: 1.005em 0px 0.375em;">Rclone 连接 Google Drive</h2><p style="box-sizing: border-box; margin: 0.92em 0px;">与 OneDrive 不同的是，Google Drive 不需要本地 Win­dows 客户端预先进行授权获取 to­ken，而是在配置过程中进行授权。</p><p style="box-sizing: border-box; margin: 0.92em 0px;">输入<span>&nbsp;</span><code style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(17, 17, 17); padding: 0px 3px; border-radius: 3px;">rclone config</code><span>&nbsp;</span>命令，会出现以下信息，参照下面的注释进行操作。</p><p style="box-sizing: border-box; margin: 0.92em 0px;"></p><details style="box-sizing: border-box; display: block;"><summary style="box-sizing: border-box; display: list-item; cursor: pointer; outline: 0px;">点击查看</summary></details><p style="box-sizing: border-box; margin: 0.92em 0px;"></p><h2 id="toc_6" style="box-sizing: border-box; font-family: &quot;PingFang SC&quot;, &quot;Hiragino Sans GB&quot;, &quot;Microsoft Yahei&quot;, &quot;WenQuanYi Micro Hei&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;, Helvetica, Arial, -apple-system, system-ui, sans-serif; color: rgb(206, 206, 207); position: relative; font-size: 1.5em; margin: 1.005em 0px 0.375em;">使用教程</h2><p style="box-sizing: border-box; margin: 0.92em 0px;">配置完成后你可以去看<span>&nbsp;</span><a href="https://p3terx.com/tag/rclone/" target="_blank" one-link-mark="yes" style="box-sizing: border-box; background-color: transparent; text-decoration: none; border-top: none rgb(144, 144, 144); border-right: none rgb(144, 144, 144); border-bottom: 1px solid rgb(144, 144, 144); border-left: none rgb(144, 144, 144); border-image: initial; color: rgb(176, 176, 176); outline: 0px; overflow-wrap: break-word; word-break: break-all;">Rclone 相关使用教程</a><span>&nbsp;</span>来了解 Rclone 更多进阶使用技巧。</p><h2 id="toc_7" style="box-sizing: border-box; font-family: &quot;PingFang SC&quot;, &quot;Hiragino Sans GB&quot;, &quot;Microsoft Yahei&quot;, &quot;WenQuanYi Micro Hei&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;, Helvetica, Arial, -apple-system, system-ui, sans-serif; color: rgb(206, 206, 207); position: relative; font-size: 1.5em; margin: 1.005em 0px 0.375em;">参考</h2><p style="box-sizing: border-box; margin: 0.92em 0px;"><a href="https://p3terx.com/go/aHR0cHM6Ly9yY2xvbmUub3JnL2RvY3Mv" target="_blank" one-link-mark="yes" style="box-sizing: border-box; background-color: transparent; text-decoration: none; border-top: none rgb(144, 144, 144); border-right: none rgb(144, 144, 144); border-bottom: 1px solid rgb(144, 144, 144); border-left: none rgb(144, 144, 144); border-image: initial; color: rgb(176, 176, 176); outline: 0px; overflow-wrap: break-word; word-break: break-all;">rclone 官方手册</a></p><p style="box-sizing: border-box; margin: 0.92em 0px;"><a href="https://p3terx.com/go/aHR0cHM6Ly93d3cubW9lcmF0cy5jb20vYXJjaGl2ZXMvNDkxLw==" target="_blank" one-link-mark="yes" style="box-sizing: border-box; background-color: transparent; text-decoration: none; border-top: none rgb(144, 144, 144); border-right: none rgb(144, 144, 144); border-bottom: 1px solid rgb(144, 144, 144); border-left: none rgb(144, 144, 144); border-image: initial; color: rgb(176, 176, 176); outline: 0px; overflow-wrap: break-word; word-break: break-all;">在 Debian/Ubuntu 上使用 rclone 挂载 OneDrive 网盘</a></p><blockquote class="content-copyright" style="box-sizing: border-box; margin: 50px -15px 0px; border-width: 4px; border-left-style: solid; border-color: rgba(255, 255, 255, 0.05) rgba(255, 255, 255, 0.05) rgba(255, 255, 255, 0.05) rgb(255, 128, 128); padding: 1px 20px; color: rgb(170, 170, 170); font-style: normal; font-size: 17.1px;"><p class="content-copyright" style="box-sizing: border-box; margin: 0.92em 0px;"><strong style="box-sizing: border-box; font-weight: 700; color: rgb(206, 206, 207);">本文作者：</strong><a href="https://p3terx.com/" target="_blank" one-link-mark="yes" style="box-sizing: border-box; background-color: transparent; text-decoration: none; border-top: none rgb(144, 144, 144); border-right: none rgb(144, 144, 144); border-bottom: 1px solid rgb(144, 144, 144); border-left: none rgb(144, 144, 144); border-image: initial; color: rgb(170, 170, 170); outline: 0px; overflow-wrap: break-word; word-break: break-all;">P3TERX</a></p><p class="content-copyright" style="box-sizing: border-box; margin: 0.92em 0px;"><strong style="box-sizing: border-box; font-weight: 700; color: rgb(206, 206, 207);">本文链接：</strong><a class="content-copyright" href="https://p3terx.com/archives/rclone-installation-and-configuration-tutorial.html" target="_blank" one-link-mark="yes" style="box-sizing: border-box; background-color: transparent; text-decoration: none; border-top: none rgb(144, 144, 144); border-right: none rgb(144, 144, 144); border-bottom: 1px solid rgb(144, 144, 144); border-left: none rgb(144, 144, 144); border-image: initial; color: rgb(170, 170, 170); outline: 0px; overflow-wrap: break-word; word-break: break-all;">https://p3terx.com/archives/rclone-installation-and-configuration-tutorial.html</a></p><p class="content-copyright" style="box-sizing: border-box; margin: 0.92em 0px;"><strong style="box-sizing: border-box; font-weight: 700; color: rgb(206, 206, 207);">版权声明：</strong>本博客所有文章除特别声明外，均采用<span>&nbsp;</span><a href="https://p3terx.com/go/aHR0cHM6Ly9jcmVhdGl2ZWNvbW1vbnMub3JnL2xpY2Vuc2VzL2J5LW5jLXNhLzQuMC9kZWVkLnpo" target="_blank" one-link-mark="yes" style="box-sizing: border-box; background-color: transparent; text-decoration: none; border-top: none rgb(144, 144, 144); border-right: none rgb(144, 144, 144); border-bottom: 1px solid rgb(144, 144, 144); border-left: none rgb(144, 144, 144); border-image: initial; color: rgb(170, 170, 170); outline: 0px; overflow-wrap: break-word; word-break: break-all;">CC BY-NC-SA 4.0</a><span>&nbsp;</span>许可协议。非商业转载及引用请注明出处（作者、原文链接），商业转载请联系作者获得授权。</p></blockquote></details>

[Linux](https://p3terx.com/tag/Linux/)[VPS](https://p3terx.com/tag/VPS/)[Rclone](https://p3terx.com/tag/rclone/)[OneDrive](https://p3terx.com/tag/OneDrive/)[Google Drive](https://p3terx.com/tag/Google-Drive/)

[ENJOY 0](javascript:void(0);) 

[Rclone 进阶使用教程 - 常用命令参数详解](https://p3terx.com/archives/rclone-advanced-user-manual-common-command-parameters.html)

[从零开始学 Git 的基础操作](https://p3terx.com/archives/learn-the-basics-of-git-from-scratch.html)

1. [前言](https://p3terx.com/archives/rclone-installation-and-configuration-tutorial.html#toc_0)
2. [安装 Rclone](https://p3terx.com/archives/rclone-installation-and-configuration-tutorial.html#toc_1)
3. Rclone 连接 OneDrive
   1. [获取 token](https://p3terx.com/archives/rclone-installation-and-configuration-tutorial.html#toc_3)
   2. [配置 Rclone](https://p3terx.com/archives/rclone-installation-and-configuration-tutorial.html#toc_4)
4. [Rclone 连接 Google Drive](https://p3terx.com/archives/rclone-installation-and-configuration-tutorial.html#toc_5)
5. [使用教程](https://p3terx.com/archives/rclone-installation-and-configuration-tutorial.html#toc_6)
6. [参考](https://p3terx.com/archives/rclone-installation-and-configuration-tutorial.html#toc_7)

### 添加新评论





OωO

提交评论



### 已有 2 条评论

![kedup](https://secure.gravatar.com/avatar/2739bcc11d340116d4840e0198beaddc?s=64&r=G&d=)**kedup**

[2019-12-02 11:03](https://p3terx.com/archives/rclone-installation-and-configuration-tutorial.html/comment-page-1#comment-293) [ 0 ](javascript:void(0))[ 0](javascript:void(0))

client_secret> # 留空，回车 之后多了
Optional - needed only for list/create/delete buckets - see your developer console.
Enter a string value. Press Enter for the default ("").
project_number>
这个怎么输入

[回复](https://p3terx.com/archives/rclone-installation-and-configuration-tutorial.html/comment-page-1?replyTo=293#respond-post-57)

![P3TERX](https://secure.gravatar.com/avatar/c42fdfa8aca47ec27a7c35dfa7d1dc51?s=64&r=G&d=)**[P3TERX](https://p3terx.com/go/aHR0cDovL3AzdGVyeC5jb20=)** 回复 **@kedup**

[2019-12-02 12:19](https://p3terx.com/archives/rclone-installation-and-configuration-tutorial.html/comment-page-1#comment-294) [ 0 ](javascript:void(0))[ 0](javascript:void(0))

没遇到过这个情况，建议你从头开始

[回复](https://p3terx.com/archives/rclone-installation-and-configuration-tutorial.html/comment-page-1?replyTo=294#respond-post-57)

© 2020 P3TERX ZONE

感谢陪伴：1320 天 12 小时 56 分 23 秒

Powered by [Typecho](http://typecho.org/) • [Theme VOID](https://blog.imalan.cn/archives/247/)

[Telegram 频道](https://p3terx.com/go/aHR0cHM6Ly90Lm1lL1AzVEVSWF9aT05F) • [Telegram 群组](https://p3terx.com/go/aHR0cHM6Ly90Lm1lL2pvaW5jaGF0L0Q3WjVUVThSdzBwOGRDLWo2YWhvZnc=)







## 配置自动上传脚本

[Aria2 一键安装管理脚本 增强版](https://p3terx.com/go/aHR0cHM6Ly9naXRodWIuY29tL1AzVEVSWC9hcmlhMi5zaA==) 整合了 [Aria2 完美配置](https://p3terx.com/go/aHR0cHM6Ly9naXRodWIuY29tL1AzVEVSWC9hcmlhMl9wZXJmZWN0X2NvbmZpZw==) ，安装后会附带一些附加功能脚本功能脚本，RCLONE 自动上传脚本就是其中之一。由于默认不启用，所以需要手动启用。

> **TIPS:** 本项目的上传脚本使用更稳定快速的原生命令上传方式，而非处在测试阶段的挂载方式，这点和一般的脚本不同。

- 输入`nano /root/.aria2c/aria2.conf`打开 Aria2 配置文件进行修改。或使用[Aria2 一键安装管理脚本 增强版](https://p3terx.com/go/aHR0cHM6Ly9naXRodWIuY29tL1AzVEVSWC9hcmlhMi5zaA==)中的手动修改选项打开配置文件进行修改。找到“下载完成后执行的命令”，把`clean.sh`替换为`upload.sh`。

```none
# 下载完成后执行的命令
on-download-complete=/root/.aria2c/upload.sh
```

> nano 编辑器的操作方法参见《[Linux 下适合新手的文本编辑器 nano 使用教程](https://p3terx.com/archives/linux-nano-tutorial.html)》

- 输入`nano /root/.aria2c/script.conf`打开附加功能脚本配置文件进行修改，有中文注释，按照自己的实际情况进行修改，第一次使用只建议修改网盘名称。

```none
# 网盘名称(RCLONE 配置时填写的 name)
drive-name=OneDrive
```

- 重启 Aria2 。脚本选项重启或者执行以下命令：

```none
service aria2 restart
```

## 检查是否配置成功

执行 `upload.sh` 脚本，提示 `success` 即配置成功。

```none
/root/.aria2c/upload.sh
```