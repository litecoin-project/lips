## Summary

The wallet released with litecoin core (and of course bitcoin) is due for an upgrade.  Currently the wallet is very outdated in style and [a redesign has been proposed](https://medium.com/litecoin-foundation/redesigning-litecoin-core-with-lightning-capabilities-3a8ebbea590a).

The proposal shows some modern design techniques which will be difficult to implement in the existing wallet.  This proposal outlines an updated web-based wallet running on top of the node.  Long term this would be hopefully a proposal to make back to Bitcoin core to replace the existing wallet but for now assume this is ancillary to core.

## Front-end

The wallet will be written in modern JavaScript and HTML with SASS for the styling.  Initially this will be written with Aurelia ([a JavaScript framework](http://aurelia.io/)) for speed of development and because it is most spec compliant and would be easiest to port to any other framework or back to vanilla.js.  Long-term the technology stack used should be determined by what will be easiest to maintain for a given period of time.

## Mid-tier

To handle abstracting out interactions with the node a simple node.js API can be used to proxy requests to the node.  This should speed up development as well.  I'm fairly lenient on this portion of the proposal.

[litecoind-rpc](https://github.com/litecoin-project/litecoind-rpc) can be used but probably needs to expose a RESTful interface or the web wallet would need to use something like electron so that the node environment can be used as well.

## Timeline / Milestones

1. Design - design assets created - done
2. Develop - develop working proof of concept - in progress
3. Review / Approval of functionality by Litecoin core maintainers
4. Develop - Start to Productionize the wallet
5. Submit a production-ready PR
6. Submit a proposal back to Bitcoin core for the same wallet

## Requirements

- Internationalization support (ex. English / Spanish)
- Accessible (ex. Screen reader friendly)
- ?
