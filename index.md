<div id="walletID"></div>
<script>
if (typeof window.ethereum !== "undefined") {
    ethereum
      .request({ method: "eth_requestAccounts" })
      .then((accounts) => {
        const [account] = accounts;

        walletID.innerHTML = `Wallet connected: ${account}`;
      })
} else {
      window.open("https://metamask.io/download/", "_blank");
}
</script>