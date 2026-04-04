<p align="center">
  <img src="https://piratetok.boats/logo1_1_alpha.png" alt="PirateTok" width="320" />
</p>

<h3 align="center">TikTok Live, unchained.</h3>

<p align="center">
  Real-time TikTok Live events in 12 languages. No signing server. No API keys. No proprietary middleman.
</p>

---

## What is this?

Every TikTok Live connector library on the internet funnels your traffic through a proprietary signing server — a black box that mints authentication tokens and gates access behind infrastructure you don't control. They'll tell you it's required. It isn't.

PirateTok libraries connect directly to TikTok's WebSocket stream. No signing server. No middleman. No fees.

12 native implementations. Same protocol. Same events. Same freedom.

## Libraries

| Language | Install | Repo |
|:---------|:--------|:-----|
| **Rust** | `cargo add piratetok-live-rs` | [live-rs](https://github.com/PirateTok/live-rs) |
| **Go** | `go get github.com/PirateTok/live-go` | [live-go](https://github.com/PirateTok/live-go) |
| **Python** | `pip install piratetok-live-py` | [live-py](https://github.com/PirateTok/live-py) |
| **JavaScript** | `npm install piratetok-live-js` | [live-js](https://github.com/PirateTok/live-js) |
| **C#** | `dotnet add package PirateTok.Live` | [live-cs](https://github.com/PirateTok/live-cs) |
| **Java** | `com.piratetok:live` | [live-java](https://github.com/PirateTok/live-java) |
| **Lua** | `luarocks install piratetok-live-lua` | [live-lua](https://github.com/PirateTok/live-lua) |
| **Elixir** | `{:piratetok_live, "~> 0.1"}` | [live-ex](https://github.com/PirateTok/live-ex) |
| **Dart** | `dart pub add piratetok_live` | [live-dart](https://github.com/PirateTok/live-dart) |
| **C** | `#include "piratetok.h"` | [live-c](https://github.com/PirateTok/live-c) |
| **PowerShell** | `Install-Module PirateTok.Live` | [live-ps1](https://github.com/PirateTok/live-ps1) |
| **Shell** | `bpkg install PirateTok/live-sh` | [live-sh](https://github.com/PirateTok/live-sh) |

## Features

- **No signing server** — no proprietary token minting, no third-party dependency
- **Auto-reconnect** — stale detection, exponential backoff, self-healing on blocks
- **Proxy support** — HTTP/HTTPS/SOCKS5
- **CDN selection** — EU, US, or Global endpoints
- **No `protoc`** — no build-time protobuf tooling, ever
- **Age-restricted rooms** — event streaming works out of the box, no special auth needed
- **Room info** — optional `fetch_room_info` call returns title, viewer count, FLV stream URLs (5 quality tiers). Age-restricted streams need session cookies for this call only — event streaming never needs cookies.

## Decode Matrix

Enriched user data on every event — badges, gifter level, moderator status, fan club, follow info.

| Event | Ours | Go | C# | JS | Python | Java |
|:------|:----:|:--:|:--:|:--:|:------:|:----:|
| `ChatMessage` | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| `GiftMessage` | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| `LikeMessage` | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| `MemberMessage` | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| `SocialMessage` | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| `RoomUserSeqMessage` | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| `ControlMessage` | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| `LiveIntroMessage` | :white_check_mark: | :x: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :x: |
| `RoomMessage` | :white_check_mark: | :x: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :x: |
| `CaptionMessage` | :white_check_mark: | :x: | :x: | :x: | :white_check_mark: | :x: |
| `GoalUpdateMessage` | :white_check_mark: | :x: | :x: | :x: | :white_check_mark: | :x: |
| `ImDeleteMessage` | :white_check_mark: | :x: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :x: |
| `RankUpdateMessage` | :white_check_mark: | :x: | :white_check_mark: | :x: | :white_check_mark: | :x: |
| `PollMessage` | :white_check_mark: | :x: | :white_check_mark: | :x: | :white_check_mark: | :x: |
| `EnvelopeMessage` | :white_check_mark: | :x: | :x: | :x: | :white_check_mark: | :x: |
| `RoomPinMessage` | :white_check_mark: | :x: | :x: | :x: | :white_check_mark: | :x: |
| `LinkMicBattle` | :white_check_mark: | :x: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| `LinkMicArmies` | :white_check_mark: | :x: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| `EmoteChatMessage` | :white_check_mark: | :x: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| `QuestionNewMessage` | :white_check_mark: | :white_check_mark: | :x: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| `SubNotifyMessage` | :white_check_mark: | :x: | :white_check_mark: | :x: | :white_check_mark: | :white_check_mark: |
| `BarrageMessage` | :white_check_mark: | :x: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| `HourlyRankMessage` | :white_check_mark: | :x: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :x: |
| `MsgDetectMessage` | :white_check_mark: | :x: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :x: |
| `LinkMicFanTicketMethod` | :white_check_mark: | :x: | :x: | :white_check_mark: | :white_check_mark: | :x: |
| `RoomVerifyMessage` | :white_check_mark: | :x: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :x: |
| `OecLiveShoppingMessage` | :white_check_mark: | :x: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :x: |
| `GiftBroadcastMessage` | :white_check_mark: | :x: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :x: |
| `RankTextMessage` | :white_check_mark: | :x: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :x: |
| `UnauthorizedMemberMessage` | :white_check_mark: | :x: | :x: | :x: | :white_check_mark: | :x: |
| `GiftPanelUpdateMessage` | :white_check_mark: | :x: | :x: | :x: | :x: | :x: |
| `InRoomBannerMessage` | :white_check_mark: | :x: | :x: | :x: | :x: | :x: |
| `GuideMessage` | :white_check_mark: | :x: | :x: | :x: | :x: | :x: |
| `GiftDynamicRestrictionMessage` | :white_check_mark: | :x: | :x: | :x: | :x: | :x: |
| `ViewerPicksUpdateMessage` | :white_check_mark: | :x: | :x: | :x: | :x: | :x: |
| + 25 Tier B events | :white_check_mark: | :x: | partial | partial | stub | :x: |
| Unknown passthrough | :white_check_mark: | :x: | :x: | :x: | :x: | :x: |
| **Signing server required** | **No** | **Yes** | **Yes** | **Yes** | **Yes** | **Yes** |

*"Ours" = all 12 PirateTok libraries. Others columns show their single upstream equivalent.*

## License

Every library is [0BSD](https://opensource.org/license/0bsd) — do whatever you want with it. No attribution required. No restrictions. No copyleft. Nothing.

---

<details>
<summary><b>The Saga</b> — why this project exists</summary>

<br/>

I joined the TikTok Live open-source community as the maintainer of the Rust library. The ecosystem was built around a single chokepoint: a proprietary signing server. Every library in every language depended on this one piece of infrastructure to function. A free community tier existed (up to 1,000 requests/day), with paid plans above that — but either way, it was a central point of failure that no one controlled except its owner.

I run an NGO that fights child sexual abuse online. TikTok, to their credit, is one of the fastest platforms to act when authorities reach out — they take these reports seriously and respond quickly, which is more than can be said for most. But reactive enforcement has limits. By the time a report is filed, the damage is done. Our work is proactive: we monitor TikTok Live streams where predators target minors, gather evidence, and intervene before abuse happens rather than after.

This kind of surveillance requires volume — far more than the community tier could offer. I couldn't afford to depend on infrastructure I didn't control for work this critical. So I built my own signing server. And while optimizing it, I discovered something: **the signing server is unnecessary**. The entire authentication ceremony — `x_bogus`, `msToken`, session tokens — none of it is validated at the WebSocket level. You don't need any of it.

I rewrote everything from scratch. Then I did it again in 11 more languages.

Every library is 0BSD. No signing server. No API keys. No gatekeepers. No one gets to sit between you and a WebSocket connection and decide whether your use case is worthy.

</details>

---

<h3 align="center">Come aboard :pirate_flag:  </h3>

<p align="center">
  <img src="https://piratetok.boats/footer.png" alt="PirateTok" width="100%" />
</p>
