# mcwiseman97's Umbrel App Store

A personal [Umbrel](https://umbrel.com) community app store.

## Add to Umbrel

1. Open your Umbrel dashboard
2. Go to **App Store** → **Community App Stores**
3. Paste this URL and click **Add**:
   ```
   https://github.com/mcwiseman97/mcwiseman97-umbrel-app-store
   ```

## Apps

### FitTrack
> Self-hosted workout & nutrition tracker

A sleek fitness tracking app for your home server. Log workouts with sets/reps/weight, track macros and calories, build custom routines, and review your progress over time — all without sending data to any third party.

**Features:**
- Workout logging with rest timer, personal-best detection, and progress charts
- Nutrition diary with custom foods, macro targets, and daily summaries
- Consistency heatmap and dashboard overview
- Full JSON + CSV data export / import
- Dark-mode-first UI optimised for phone and desktop

**Image:** [`ghcr.io/mcwiseman97/fittrack`](https://github.com/mcwiseman97/mcwiseman97-umbrel-app-store/pkgs/container/fittrack)
**Port:** 3080

---

## Development

To build and push a new version of FitTrack:

```bash
# Build
cd fittrack-source/
docker build -t ghcr.io/mcwiseman97/fittrack:<version> .

# Push
echo <PAT> | docker login ghcr.io -u mcwiseman97 --password-stdin
docker push ghcr.io/mcwiseman97/fittrack:<version>
```

Then update `version:` and `image:` in `mcwiseman97-umbrel-app-store-fittrack/umbrel-app.yml` and `mcwiseman97-umbrel-app-store-fittrack/docker-compose.yml`.
