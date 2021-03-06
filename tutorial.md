https://github.com/regen-network/testnets/blob/master/aplikigo-1/README.md#regen-network-testnet-aplikigo-1-testnet

1. In the above official tutorial, when you install go-1.15.5, you may get an error when you execute "go version" after the installation, because you did not add environment variables. You can find how to add environment variables in another tutorial.

```
  $ echo "" >> ~/.bashrc
  $ echo 'export GOPATH=$HOME/go' >> ~/.bashrc
  $ echo 'export GOROOT=/usr/local/go' >> ~/.bashrc
  $ echo 'export GOBIN=$GOPATH/bin' >> ~/.bashrc
  $ echo 'export PATH=$PATH:/usr/local/go/bin:$GOBIN' >> ~/.bashrc

  $ source ~/.bashrc
```

2.If you have created an address before and want to import the wallet you created before, you need to execute the following command:

```
$ regen init --chain-id=aplikigo-1 <your_moniker>
$ regen keys add <your_wallet_name> --recover
```

3.After generating the Json file, perform the following operations to successfully submit Gentx.

```
git clone https://github.com/<your-github-username>/testnets
cd testnets/
git add aplikigo-1/gentxs/<your_gentx_file.json>
git commit -m 'add gentx'
git push origin master
```

Then enter your github username and github password. Finally, do the following:

①.Enter "https://github.com/<your-github-username>/testnets" and click "Pull request".

② click "Create pull request".

③click "Create pull request".