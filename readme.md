##TEST FURKAN##

# Liquidity Health Dashboard Configuration Repo

Welcome to the Liquidity Health Dashboard integration guide! We're excited to have you on board as we strive to provide smooth and seamless liquidity tracking for your project. We've designed this README to be informative, engaging, and easy to follow for everyone. Let's dive right in!

## Table of Contents

- [Overview](https://github.com/efeDaniels/lhd-readme-example#overview)
- [Getting Started](https://github.com/efeDaniels/lhd-readme-example#getting-started)
- [How to Submit a PR ?](https://github.com/efeDaniels/lhd-readme-example#how-to-submit-a-pr-)
- [Deployment Example](https://github.com/efeDaniels/lhd-readme-example#deployment-example)
- [FAQs](https://github.com/efeDaniels/lhd-readme-example#faq)
- [Support](https://github.com/efeDaniels/lhd-readme-example#support)

## Overview

At ApeSwap, we understand the importance of accurate and reliable liquidity tracking for projects. Our platform provides a comprehensive solution for tracking web3 projects' liquidity, ensuring that it's team can focus on what matters most - building and growing project. By following this guide, you'll be able to easily integrate your project with our platform and enjoy all the benefits that come with it.

## Getting Started

Before you dive into submitting a PR, ensure you have the following prerequisites in place:

1.  A Github account to create and submit PRs.

2.  A local environment set up with `Node.js` and `yarn` installed.

3.  Fork our repository to your own Github account.

Now, you're ready to submit your PR!

## How to Submit a PR ?

Submitting a PR is as simple as following these steps:

1. **Clone the repository:** Clone your forked repository to your local environment.

2. **Install packages:** Navigate to the project folder and run `yarn` to install all applicable packages.

3. **Edit the `.ts` file:** Locate and edit the applicable `.ts` file inside the config folder. Make sure to provide all the necessary information about your project.

4. **Run configuration:** Run `yarn configure` to convert your TypeScript entry into a consumable JSON file.

5. **Commit and push:** Commit your changes and push them to your forked repository.

6. **Submit a PR:** Create a new pull request in our `main` repository, targeting the main branch.

And voilà! Your PR is submitted, and our team will review and merge it as soon as possible. EEEEE

## Deployment Example

In that example, we'll add our native token BANANA to the repo! We'll need to go `src > constants` folder and open `addresMappingWhitelist.ts`. And you'll notice skeleton of code block looks like that:

```bash
{
    tokenSymbol: '',
    tokenName: '',
    tokenLogoUrl: '',
    tokenAddresses: [
      { address: '', chainId: '' },
      { address: '', chainId: '' },
    ],
    knownOwners: [
      '',
      '',
      '',
    ],
},
```

Once you finish filling, it should look like that:

```bash
 {
    tokenSymbol: 'BANANA',
    tokenName: 'ApeSwap BANANA',
    tokenLogoUrl: 'https://raw.githubusercontent.com/ApeSwapFinance/apeswap-token-lists/main/assets/BANANA.svg',
    tokenAddresses: [
      { address: '0x603c7f932ed1fc6575303d8fb018fdcbb0f39a95', chainId: '56' },
      { address: '0xd978f8489e1245568704407a479a71fcce2afe8f', chainId: '42161' },
    ],
    knownOwners: [
      '0x944694417a6ca0a70963d644a11d42c10e3af042',
      '0xabd7853b79e488bc1bd9e238a870167b074eb714',
      '0x71c0c1001520e1568e17836cc8a19d0dbdb2bd5f',
    ],
  },
```

**Be Aware Of Those Importnat Details:** 

`tokenSymbol` has to be always uppercase.

All contract addresses should be lowercase at contract address needed variables such as  `tokenAddresses`, `knownOwners`.

`knownOwners` should be a known liquidity holder wallet of the project. That can be a GnosisSafeProxy wallet or a locking contract etc.

Please don't forget to use  `Prettier` before comitting your code.

Once you finish the code, run `yarn configure` to convert your TypeScript entry into a consumable JSON file and create a new pull request in our main repository.

## FAQ

#### Q: What if I encounter issues during the PR process?

A: Don't worry! Our team is here to help. Feel free to reach out to us via our [Support](https://github.com/efeDaniels/lhd-readme-example#support) channels, and we'll be happy to assist you.

#### Q: How long does it take for my PR to be reviewed and merged?

A: We aim to review and merge PRs as quickly as possible. Please allow our team up to 3 business days to process your request.

#### Q: What happens after my PR is merged?

A: Congratulations! Your project is now integrated with our liquidity tracking product. You can start monitoring your liquidity and leveraging our tools to make informed decisions for your project.

## Support

We're committed to providing you with the best support possible. If you have any questions, issues, or concerns, feel free to reach out to us through the following channels:

- [Discord](https://discord.com/invite/ApeSwap)

- [Telegram](https://t.me/ape_swap)

Thank you for choosing ApeSwap! We're looking forward to working with you and helping your project thrive.
