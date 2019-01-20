# DogePrivate-DGP

<h2>Requirements</h2>
				<ul>
				  <li>Windows 7 or higher (as your Cold wallet)</li>
				  <li>Linux VPS (Ubuntu 16.04 64 bit) that running 24/7 such as <a href="https://www.vultr.com/?ref=7426137" rel="nofollow" target="top">Vultr (stable and cheap host)</a>, or other VPS provider (as your Hot wallet)</li>
				  <li>SSH client, to connect to Linux VPS. Recommend <a href="https://putty.org" rel="nofollow" target="_blank">PuTTY</a></li>
				</ul>
				<h2 style="color: #25499A">Part 1: Windows Cold Wallet Installation</h2>
				<p>NOTED:</p>
				<ul>
				  <li>Required to send 10,000 DOGP into this wallet as MasterNode collateral, so we need about 10,005 DOGP in our wallet because of some fee transaction</li>
				  <li>This wallet will be the one that receive the MasterNode rewards</li>
				  <li>It DOES NOT need to run 24/7</li>
				</ul>
<p>&nbsp;</p>				
				<h3><ol start="1"><li>Install and run the dogecoinprivate-qt wallet on your Windows machine</li></ol></h3>
					<li>Download dogecoinprivate-qt the latest wallet <br>
  Windows Wallet (32 bit): https://github.com/PrivateDOGP/DOGP-Project/releases/download/v1.0.0/dogecoinprivate-win32.zip
  </br>
  Windows Wallet (64 bit): https://github.com/PrivateDOGP/DOGP-Project/releases/download/v1.0.0/dogecoinprivate-win64.zip 
					</li>
					<li>Extract wallet </li>
					<li>Double  click on <strong>dogecoinprivate-qt</strong> to install wallet</li>
					<li>Click  &quot;Yes&quot; button if you get 'unknown publisher' warning to continue</li>
					<li>If  you first time run the wallet, a pop-up screen will prompt for Data Directory.  By default, it will store in AppData\roaming\DOGP directory.</li>
					<li>Let  the wallet sync until you see the tick symbol on the right bottom</li>
					<p><img src="https://raw.githubusercontent.com/cryptosam212/DogePrivate-DGP/master/wallet1.png" width="1000px" style="margin:10px"></p>
					<h3><ol start="2">
				  <li>
				   Create a wallet address and send DOGP coin to the address for your MasterNode collateral.
				  </li>
				</ol></h3>
				<ol>
				  <ol type="a">
					<li>From  the top menu, go to <strong>File</strong> -&gt;  Receiving addresses</li>
					<li>Click  on &quot;<strong>New</strong>&quot; button, enter a  label (for example, MN1) and click on &quot;OK&quot; button<br>
					<img src="https://raw.githubusercontent.com/cryptosam212/DogePrivate-DGP/master/wallet2.jpg" width="1000px" style="margin:10px">
					</li>
					<li>Select on the newly created wallet address from the list and then click on "Copy" button to copy the address into the clipboard</li>
					<li>Send exactly 10,000 DOGP coins to the address that you just copied. Ensure the address is correct before you send out the coin.</li>
					<li>After coin is sent out, you can verify the balance in the 'Transactions' tab and wait for at least 15 confirmations to validate your transaction (it usually takes about 30 minutes).</li>
				  </ol>
				</ol>

<h3><ol start="3">
	  <li>Obtain transaction of the collateral transfer information.
 </li>
</ol></h3>
<ol>
  <ol type="a">
					<li>From the top menu, go to Tools -&gt;Debug console</li>
					<li>Run following command:   <span style="font-size:16px; background-color:#86BBE1; padding:3px 5px 3px 5px; font-weight:bold">masternode outputs</span><br>
				<img src="https://raw.githubusercontent.com/cryptosam212/DogePrivate-DGP/master/wallet4.jpg" width="1000px" style="margin:10px">
				<br>
					</li>
					
</ol>
				</ol>
				<p>&nbsp;</p>
				<h2 style="color: #25499A">Part 2: Subscribe VPS for Hot Wallet server</h2>
				<p>NOTED:<br>
				</p>
				<ul>
				  <li>We need <strong style="color:#FF0000">IPv4</strong></li>
				  <li>This server REQUIRED to run 24/7</li>
				  <li>Since running 24/7, strongly suggest not store any fund in this wallet to avoid losing fund in case server is attack.</li>
				</ul>
				<ol style="font-weight:bold">
				<p>You can subscribe VPS from provider like <a href="https://www.vultr.com/?ref=7426137" rel="nofollow" target="_blank">Vultr (stable and cheap host)</a>, or other similar providers with following requirements;</p>


<ol type="a">
	<li>
<br/>Promo Vultr, get Discount<br/>
<a href="https://www.vultr.com/?ref=7773816-4F"><img src="https://www.vultr.com/media/banner_2.png" width="468" height="60"></a>
	</li>
					<li>Register an account Vultr, then click on &quot;+&quot; button from the dashboard<br>
					<img src="http://dextro.io/images/vultr1.png" width="800px" style="margin:10px">
						
</li>
					<li>Select any 'Server Location' follow by Ubuntu 16.04 x64 for 'Server Type' and $5/mo with 25 GB SSD for 'Server Size' <br>
				<img src="https://raw.githubusercontent.com/cryptosam212/sam_dxo/master/vultr2.png" width="800px" style="margin:10px">
				</li>
					<li>Enter a Hostname and Label for your VPS (for example, Dextro)<br>
				<img src="http://dextro.io/images/vultr3.png" width="800px" style="margin:10px">
				</li>
					<li>After successfully install the VPS, click on the server from the list to get and copy <strong>IP Address</strong> and <strong>root's Password</strong><br>
				<img src="http://dextro.io/images/vultr4.png" width="800px" style="margin:10px"></li>
				  </ol>
				  </ol>
				<h2 style="color: #25499A">Part 3: Linux (Ubuntu) Hot Wallet Installation</h2>
				<p>NOTED:<br>
				</p>
				<ul>
				  <li>You may use SSH client to connect the VPS. Recommend <a href="https://putty.org" rel="nofollow" target="_blank">PuTTY</a></li>
				</ul>

<ol>
				  <li>
					Launch PuTTY application and login into VPS. Copy VPS IP Address and click open.<br>
				<img src="http://dextro.io/images/putty1.png" width="500px" style="margin:10px">
				<br>
				<img src="http://dextro.io/images/putty1a.png" width="500px" style="margin:10px"><br>
				<br>
				Login as root. Copy VPS Password and paste it into PuTTY (mouse right click to paste. Password not shown and press Enter)<br>
				<img src="http://dextro.io/images/putty2.png" width="600px" style="margin:10px"><br>
				<br>

</li>
				  <li>
				  copy and paste this below code into putty<br>
				  <br>
<li>
				<span style="background-color:#666; font-weight:bold; font-size:18px; padding:10px 20px 10px 20px">wget https://raw.githubusercontent.com/cryptosam212/DogePrivate-DGP/master/install_dogp.sh && bash install_dogp.sh </span><br>
				<br>
				<img src="https://raw.githubusercontent.com/cryptosam212/DogePrivate-DGP/master/putty3.jpg" width="600px" style="margin:10px"><br><br>
				</li>
				</li>
				  <li>Add 4GB Swap. This is only for server 1024MB VPS. (OPTIONAL)<br>
				  <img src="https://raw.githubusercontent.com/cryptosam212/DogePrivate-DGP/master/add_swap4GBputty.jpg" width="600px" style="margin:10px"><br>
				<img src="https://raw.githubusercontent.com/cryptosam212/DogePrivate-DGP/master/add_swap4GBputty1.jpg" width="600px" style="margin:10px"><br>
				  </li>
				  <li>Install new dogecoinPrivate Masternode<br>
				if you quit from dogecoinprivate MN script, you can run again it with command: bash install_dogp.sh<br>
				<ol type="a">
				<li>Choose option 1 for create new masternode, and follow the instruction. <br>
					Do you want to install all needed dependencies? choose y for new vps<br/></li>
					<li>Do you want to install wallet version 100000 to usr/local/bin? choose y  for new vps<br><br></li>
				<img src="https://raw.githubusercontent.com/cryptosam212/DogePrivate-DGP/master/putty4.jpg" width="600px" style="margin:10px"><br><br>
	<img src="https://raw.githubusercontent.com/cryptosam212/DogePrivate-DGP/master/putty5.jpg" width="600px" style="margin:10px"><br>
					<li>Press enter to auto generate private key</li>
					<li>Wait untill process done</li>
					<li>to check, run masternode menu that given.</li>
					<br>
	<img src="https://raw.githubusercontent.com/cryptosam212/DogePrivate-DGP/master/putty6.jpg" width="600px" style="margin:10px"><br>
	</ol> </li>
				  <li>
					Now, we can setup masternode config. At windows wallet click 
					  <br>
					  Tools -&gt; Open Masternode Configuration File.
					  <br>
					Fill masternode code at new line like this <br>
				<img src="https://raw.githubusercontent.com/cryptosam212/DogePrivate-DGP/master/wallet5.jpg" width="1000px" style="margin:10px"></li>
				</ol>

<h2 style="color: #25499A">Part 4: Masternode Activation</h2>
				<ol>
				  <h3><li>Enable Masternode</li></h3>
				  Restart your Windows Cold Wallet. From the top menu, go to Tools -&gt; Debug console<br>
				to acivate masternode, use command <strong>startmasternode alias "0" "MN_ALIAS"</strong><br><br>

<span style="background-color:#ccc; font-weight:bold; font-size:18px; padding:10px 20px 10px 20px">startmasternode alias "0" "MN1"</span>
				<br>
				<img src="https://raw.githubusercontent.com/cryptosam212/DogePrivate-DGP/master/mn1.jpg" width="600px" style="margin:10px"><br><br>
				check at masternode tab and click update status for get newest status<br>
				<img src="https://raw.githubusercontent.com/cryptosam212/DogePrivate-DGP/master/mn2.jpg" width="600px" style="margin:10px"><br>
				if status enable, your masternode already activated. Check next 10minutes for active time must change forward.
				<br>

<h3><li>Check your MasterNode is enabled on VPS</li></h3>
				  <ol type="a">
				  <li>inside your VPS, access masternode's menu. <br></li>
<img src="https://raw.githubusercontent.com/cryptosam212/DogePrivate-DGP/master/mn3.jpg" width="600px" style="margin:10px"><br>
<br>

<img src="https://raw.githubusercontent.com/cryptosam212/DogePrivate-DGP/master/mn4.jpg" width="600px" style="margin:10px"><br>
<br>
				  </ol>
				</ol>
				<p>&nbsp;</p>  
				<p>Congratulations, your masternode has been activated and running. Just wait for your first reward.</p> </div>
							<br />
