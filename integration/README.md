# Fusion Video: integration scope

完成独立 API 图片与视频素材生成。Java 图片策略的同步返回和视频策略的状态解析需新增适配；未编译或部署原应用，未完成原生视频任务回写。

Standalone image/video assets verified. Java synchronous image strategies and video status parsing need an adapter. The original application was not built or deployed; native task write-back is unverified.

## Contract

- HTTPS origin: `https://toapis.com`, Bearer API Key; no key forwarded to assets.
- Price: `GET /v1/pricing?model=...&type=image|video`, match every catalog condition; no quote means stop.
- Create: `POST /v1/images/generations` or `/v1/videos/generations`; persist submission state before POST and ID immediately afterward.
- Poll existing ID only; `in_progress` is running; `completed` is success; failed/cancelled/expired stop.
- Result: `result.data[0].url`; validate actual image/MP4 bytes.
- Cost: only settled billing is actual; a missing image bill is not zero.

## Native work remaining

Review the Java provider/strategy image generation and video query implementations in the pinned source. Add ToAPIs image async wait and video task normalization, persist IDs and billing; do not parse the async response as synchronous OpenAI data. Native build, deployment and product flow acceptance require the maintainer’s target version and environment.

## Acceptance / 待维护者确认

Target app version and supported model presets; existing supplier/referral ownership; key storage and deployment proxy policy; quote/approval display; create/poll/result/import; refresh/restart resumes same task; actual billing and error handling. Supply test credits by agreement, with no guaranteed quota, SLA or acceptance deadline.
