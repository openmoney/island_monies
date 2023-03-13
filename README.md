# island_monies

A simple script to demonstrate the emergence of _island monies_ (a simplistic illustration of some _open money_ properties).

## Installation

This script has very few dependencies. Just run it and see what happens. The script can be run from the locally (_./islands_) or placed somewhere in the command path (e.g. _/usr/local/bin/islands_). It should run without modification on any Unix-like OS. It has not been tested on _Windows_.

When running this script for the first time, any unsatisfied _Python 3_ dependencies will be reported. Those least likely to be already present are _numpy_ and _matplotlib_.

It is also necessary to have _dot_ (_GraphViz_) installed. This script does not make use of the _PyGraphViz_ library, instead making a _system_ call to the unwrapped version.

## What it does ...

This script is very simple indeed. It loops for a specified number of times, on each pass randomly selecting two agents (a _payer_ and a _payee_) and a _payment value_ (either 1 or a randomly-selected value within a specified limit). The _agents_ are identifed by number, and if the _payer_ number and _payee_ number share a "common bond" (in this case, and in this initial version, a very simple characteristic: is the 10s digit divisible by 2, 5 or 10?) then they are assigned to an _island_ having its own _money_ (one metrically equivalent to, but not exchangeable for, _legal tender_) in which this paparticular payment will be made.

The underlying assumption here is that use of the _island money_ at this decision point offers an advantage over the use of _legal tender_. This would be the case, for example, where the _payer_ (the _buyer_) does not have quite enough _legal tender_ liquidity to complete the purchase but the _payee_ (the _seller_) can afford to accept part of the payment in an _island currency_ without incurring a risk, especially where the _island money_ (a _measure_ currency rather than a _commodifiable_ currency) offers other benefits beyond that of making a sale that would otherwise not be possible.

This version of the script generates two visualizations:
1. A plot of balances for each _island_ (demonstrating the similarity of each _island money_ balance distribution with each of the others and with that of _legal tender_), and
2. The fairly rapid emergence of a closed network of _agent_-to-_agent_ payment paths over time, demonstrating the importance of patience and persistence in building such networks.

The capabilities of the script can be seen by running _islands -h_.
