##1day
[参考にしたサイト](http://catcher-in-the-tech.net/1063/)
###vimの設定ファイル
.vimrcはvimの設定ファイルで、各ユーザのホームディレクトリ直下に.vimrcとして配置するファイルです。 
###vimのプラグイン管理

- NeoBundle install

```bash
git clone https://github.com/Shougo/neobundle.vim ~/.vim/bundle/neobundle.vim
```

- NeoBundleの基本的な使い方

```.vimrc
"---------------------------
" Start Neobundle Settings.
"---------------------------
" bundleで管理するディレクトリを指定
set runtimepath+=~/.vim/bundle/neobundle.vim/
 
 " Required:
 call neobundle#begin(expand('~/.vim/bundle/'))
  
	" neobundle自体をneobundleで管理
	NeoBundleFetch 'Shougo/neobundle.vim'
	 
	 " 今後このあたりに追加のプラグインをどんどん書いて行きます！！"
	  
		call neobundle#end()
		 
		 " Required:
		 filetype plugin indent on
		  
			" 未インストールのプラグインがある場合、インストールするかどうかを尋ねてくれるようにする設定
			" 毎回聞かれると邪魔な場合もあるので、この設定は任意です。
			NeoBundleCheck
			 
			 "-------------------------
			 " End Neobundle Settings.
			 "-------------------------
			 
			 ```
			 
###プラグインインストール
			 
			 - NERDTree
			   Vimを開いているときに編集中のファイル・ディレクトリを一覧して見ることができる
				 
######NERDTree install
				 
				 ```.vimrc
				 " Required:
				 call neobundle#begin(expand('~/.vim/bundle/'))
				  
					" neobundle自体をneobundleで管理
					NeoBundleFetch 'Shougo/neobundle.vim'
					 
					 " NERDTreeを設定                  <----- 追記
					 NeoBundle 'scrooloose/nerdtree'   <----- 追記
					  
						call neobundle#end()
						
						```
						上記設定を保存した後、再度Vimを開き直します。すると、基本設定の最終行でNeoBundleCheckを記載しているので、下記のように尋ねられます。
						
						使い方
						vimが立ち上がったらコマンドモードで:NERDTreeと入力すると表示される
						
####vimをアップデートしろといわれるので適当にググってアップデート
####gitのエディターをvimに変更
						
						```bush git config --global core.editor 'vim -c "set fenc=utf-8"'
						
						```
						  
							  
##2day
								
####neocomplcacheをインストール
								メソッドなどを自動補完してくれる
								
								インストール先のディレクトリに「doc/neocomplcache.txt」というファイルがあります。
								
								その中を「EXAMPLE」という文字で検索すると.vimrcに追記する設定例があるので、それを.vimrcに追記します。
								
								追記
								```.vimrc
								NeoBundle 'Shougo/neocomplcache'
								
								あと設定例をそのままコピー
								```
								
								
####RSenceをインストール
								rubyの自動補完、定義元にジャンプしてくれる
								(RSense ユーザーマニュアル)[http://cx4a.org/software/rsense/manual.ja.html]
								
								まずjavaをインストール
								```bash
								$ sudo yum install java-1.8.0-openjdk wget -y
								
								```
								
								RSence install
								```bash
								$ wget http://cx4a.org/pub/rsense/rsense-0.3.tar.bz2
								$ bzip2 -dc rsense-0.3.tar.bz2 | tar xvf -
								$ sudo cp -r rsense-0.3 /usr/local/lib
								$ sudo chmod +x /usr/local/lib/rsense-0.3/bin/rsense
								```
								
								インストール確認
								// バージョン番号が表示されればOK
								
								```bush
								$ /usr/local/lib/rsense-0.3/bin/rsense version
								RSense 0.3
								```
								
								
								インストールディレクトリ配下にある「etc/config.rb」を使って「 ~/.rsense」というファイルを作成します。
								
								```bush
								 ruby /usr/local/lib/rsense-0.3/etc/config.rb > ~/.rsense
								 ```
								 
								 
								 追記
								 ```.vimrc
								 NeoBundle 'taichouchou2/vim-rsense'
								 ```
								   
##3day
									 
									 あきた。。。。
									 vimはしばらくやめよう。。									   
										   
											   
												   
													   
														   
															   
																   
																	   
																		   
																			   
																				   
																					   
																						   ``````````````` " " "``" "" " " " " " " "" ""```
