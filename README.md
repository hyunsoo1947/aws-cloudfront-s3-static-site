1️⃣ Architecture
User
  ↓
Route 53 (A Alias)
  ↓
CloudFront
  ↓
S3 (Origin, OAC enabled)

2️⃣ What I Implemented
 - Configured CloudFront distribution for S3
 - Attached ACM certificate (root + www)
 - Configured Route53 A Alias records
 - Debugged 403 due to missing alternate domain
 - Validated traffic via CloudFront headers
 - Performed cache invalidation

3️⃣ Issues Faced
 - 403 error when alternate domain not included
 - Certificate mismatch error
 - Root domain not resolving (missing A Alias)
 - DNS propagation delay
 - CloudFront deployment delay

4️⃣ Lessons Learned
 - CloudFront requires alternate domain + matching certificate
 - Root and www must be configured separately in Route53
 - Disable → wait → Delete is required
 - CDN propagation delay must be considered
