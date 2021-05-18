# Terraswap Wifeswap
## Get the Luna:bLuna exchange rate on Terraswap

A few notes:

1. Currently, after the auto announcement at 5%+, the bot goes to sleep for 10min or so to avoid spam

2. This is the skeleton for an auto-swapper bot, it's just missing the actual wallet and swap, which can be added by anyone wanting to create a bot or extend this one. 

3. It simulates a swap tx every .6 seconds (to avoid overloading the API). Since it's still simulating more than 1 tx per second, it's highly unlikely that by the time you manually go on Terraswap the swap rate will be as high as announced by the bot.

4. TG commands:
  /swap simulates a tx and gives current Luna:bLuna swap rate
  /info gives some basic info about the bot's functionality:
  
          Hallo!
          I'm a simple bot.

          You can use '/swap' to get the current Luna:bLuna exchange rate on Terraswap.
          I will also alert everybody automatically when the swap rate is greater than 5% in either direction.

          NOTES
          1. My rates do not take either tx commission (it's always ~0.003%), nor slippage into account – the swap simulation on Terraswap doesn't return     slippage/minimum received. So, although the given spread is not exactly the one a real swap would have, it serves as a rough estimate!
          2. High swap rates are usually very short-lasting, often under a minute. I'm constantly simulating swaps on Terraswap to get the current exchange rate, so please don't blame me if the rate is lower by the time you make it to Terraswap!
    
5. Terraswap documentation at https://docs.terraswap.io/docs/
