# alpine-base

<!---
Note: Do NOT edit directly, this file was generated using https://github.com/chainguard-images/readme-generator
-->

[![CI status](https://github.com/chainguard-images/alpine-base/actions/workflows/release.yaml/badge.svg)](https://github.com/chainguard-images/alpine-base/actions/workflows/release.yaml)

Alpine base image built with [apko](https://github.com/chainguard-dev/apko). Uses packages from the [Alpine distribution](https://www.alpinelinux.org/).

## Get It!

The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/alpine-base:latest
```

## Supported tags

| Tag | Digest | Arch |
| --- | ------ | ---- |
| `latest` | `sha256:fadcb5272fa893fe96f59b1c1706bfbf428698adcca3aca3c7286cca95ae6c2e`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:fadcb5272fa893fe96f59b1c1706bfbf428698adcca3aca3c7286cca95ae6c2e) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration-20221119` | `sha256:b45e881509e4fe79101a62692735840ffad724b9f999cd1d587f386c446bb7e6`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:b45e881509e4fe79101a62692735840ffad724b9f999cd1d587f386c446bb7e6) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration` `migration-20221121` | `sha256:fbd159fb7d519ea5f1ef179c8a83a17eff4253fa9a179450cfbc0335be7cb85c`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:fbd159fb7d519ea5f1ef179c8a83a17eff4253fa9a179450cfbc0335be7cb85c) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `migration-20221120` | `sha256:d0bf89ec9e1e7986e76115d112234e05170253276d22169ae802a18de9029401`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:d0bf89ec9e1e7986e76115d112234e05170253276d22169ae802a18de9029401) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |


## Usage

```
docker run cgr.dev/chainguard/alpine-base echo "hello"
```

See the [examples/](./examples/) directory for how
to use this as a base image.


## Signing

All Chainguard Images are signed using [Sigstore](https://sigstore.dev)!

<details>
<br/>
To verify the image, download <a href="https://github.com/sigstore/cosign">cosign</a> and run:

```
COSIGN_EXPERIMENTAL=1 cosign verify cgr.dev/chainguard/alpine-base:latest | jq
```

Output:
```
Verification for cgr.dev/chainguard/alpine-base:latest --
The following checks were performed on each of these signatures:
  - The cosign claims were validated
  - Existence of the claims in the transparency log was verified offline
  - Any certificates were verified against the Fulcio roots.
[
  {
    "critical": {
      "identity": {
        "docker-reference": "ghcr.io/chainguard-images/alpine-base"
      },
      "image": {
        "docker-manifest-digest": "sha256:fadcb5272fa893fe96f59b1c1706bfbf428698adcca3aca3c7286cca95ae6c2e"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "8a1b56ca35de167472b29efd9087a362550b7659",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/alpine-base",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEUCIQDAqK3t/o0mCFN3ksmbIWwZxsmNLBEfc8vDB66DoGYS7AIgRPt5i+x/88zhS95MkeVAta922PyK4ysMoJ8r47bm6Ig=",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiI5YzUwZTJhNGE4NjBiZmIwZjg4MTEzNDk5N2QyZTY0ZDQ5ZTdkYWRiYTcyMDRkNWRjM2Y4NWM4OTU1ZDlhOGNlIn19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJUUNpNERDSHg0eVdNZUNKQk5qYU9rL1lrSUVGNWpnaE5VSGlseHRlbW01RSt3SWdWS2ZUc0FKdXp4aEJKU2t3OEJXSHlESGIrcGZJbmExeUNrUlU1V1haT3ZvPSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUjBha05EUVhwMVowRjNTVUpCWjBsVlRsVlBNSE56YjFSb09XMXpaR1ZXYVVwVWVsQmpjMUJ0VTJwbmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVU1hoTlJFVjNUVlJSZUZkb1kwNU5ha2w0VFZSSmVFMUVSWGhOVkZGNFYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVV6ZHpSRVNtVjFVbUZSYVUxcVUycDVRVXhoYldOTVlXYzBaVXhzUlhjMlJrcDVXRUlLVDFaWmFHUkhhVzAxWnpOamRHUnpMME55YWxCTFpHZENPRUZQYW5BM1JsTlBTWFo1Um5KSGN6RllVemhTWjJ4V01rdFBRMEZzYjNkblowcFhUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlZOWkZoVUNpOVVlRE5EWTJZME1uRnJXVmd6ZVVsSFQxaFBOVXBqZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDJKUldVUldVakJTUVZGSUwwSkhUWGRaV1ZwbVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5Um5OalIyeDFXbE14YVZsWVRteE1lVFZ1WVZoU2IyUlhTWFprTWpsNVlUSmFjMkl6WkhwTU0wcHNZa2RXYUdNeVZYVmxWMFowQ21KRlFubGFWMXA2VERKb2JGbFhVbnBNTWpGb1lWYzBkMDlSV1V0TGQxbENRa0ZIUkhaNlFVSkJVVkZ5WVVoU01HTklUVFpNZVRrd1lqSjBiR0pwTldnS1dUTlNjR0l5TlhwTWJXUndaRWRvTVZsdVZucGFXRXBxWWpJMU1GcFhOVEJNYlU1MllsUkJWMEpuYjNKQ1owVkZRVmxQTDAxQlJVTkNRV2g2V1RKb2JBcGFTRlp6V2xSQk1rSm5iM0pDWjBWRlFWbFBMMDFCUlVSQ1EyYzBXVlJHYVU1VVdtcFpWRTB4V2tkVmVFNXFZekJPZWtwcFRXcHNiRnB0VVRWTlJHY3pDbGxVVFRKTmFsVXhUVWRKTTA1cVZUVk5RbmRIUTJselIwRlJVVUpuTnpoM1FWRlJSVVJyVG5sYVYwWXdXbE5DVTFwWGVHeFpXRTVzVFVOelIwTnBjMGNLUVZGUlFtYzNPSGRCVVZWRlNGZE9iMWxYYkhWYU0xWm9ZMjFSZEdGWE1XaGFNbFo2VERKR2MyTkhiSFZhVXpGcFdWaE9iRTFDTUVkRGFYTkhRVkZSUWdwbk56aDNRVkZaUlVRelNteGFiazEyWVVkV2FGcElUWFppVjBad1ltcERRbWxuV1V0TGQxbENRa0ZJVjJWUlNVVkJaMUk0UWtodlFXVkJRakpCVGpBNUNrMUhja2Q0ZUVWNVdYaHJaVWhLYkc1T2QwdHBVMncyTkROcWVYUXZOR1ZMWTI5QmRrdGxOazlCUVVGQ2FFcGxNR2hUYTBGQlFWRkVRVVZqZDFKUlNXZ0tRVXN3WkZGVVZXcG5hVUZxTmxWNWMwcGhNRFJMTmtkRWNUWjNNWFZQTVhOUmNHZFpZWGc0ZDNoYVRYTkJhVUpyYnl0eVNscENhVGw2SzFZM1lWTlNTQXBhUmpaelVsZEJXVWt4YTFVNFZ6Qm9USEZTV2psclozQTVSRUZMUW1kbmNXaHJhazlRVVZGRVFYZE9jRUZFUW0xQmFrVkJkemxMVTNOUk5tNUlaamgyQ2pnMWNYTnRSV1F3TkZVclVqZ3hSVkJzZWxRM1VFVTBVeko1TVVKTFRHWXJlWHBVZUdGYVJFUnFkV2x1Vm5oSFYyUkVTbEpCYWtWQk9WTnlja3hXYWxNS2NWaENORm92YVhCemMzWnpZamc0T1Vkd2JUZGpjME5CVFZnM1NGRXpUa05wUnk5VFYwTXZjaXRrYURWVE4waGhNR0ZFT1UxWVVtVUtMUzB0TFMxRlRrUWdRMFZTVkVsR1NVTkJWRVV0TFMwdExRbz0ifX19fQ==",
          "integratedTime": 1668992525,
          "logIndex": 7507416,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/alpine-base/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/alpine-base",
      "githubWorkflowSha": "8a1b56ca35de167472b29efd9087a362550b7659",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3510584579",
      "sha": "8a1b56ca35de167472b29efd9087a362550b7659"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

