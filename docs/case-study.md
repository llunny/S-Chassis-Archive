# Case Study — S-Chassis Archive

## Problem
Legacy S-chassis registries were the primary source for VIN/frame decoding and production rarity data. When they went dark or became unreliable, the community lost access to vital OEM information.

## Goals
- Build a modern S13/S14/S15 VIN/frame decoder
- Preserve production counts and rarity context
- Make results fast, searchable, and easy to understand
- Maintain correctness through validation and repeatable parsing

## Solution
I built a data pipeline in Python to parse OEM EPC records, normalize Nissan codes across years/markets, and aggregate production by grade, options, and colourways. The resulting datasets power a Vite/React frontend and Supabase backend.

## Architecture
- Frontend: Vite + React + TypeScript + Tailwind + shadcn/ui
- Backend: Supabase (Postgres + auth + edge functions)
- Hosting: Porkbun (domain + deployment)

## Impact
- Replaced lost registry functionality with a modern alternative
- Centralized production and colourway rarity data
- Created a platform that can grow with community verification

## Lessons Learned
- Normalization and validation matter more than scraping volume
- Community feedback is the best correctness test
- Data provenance needs to be preserved from day one

## Next Steps
- Special editions and market-exclusive trims
- Deeper EPC part-number linkage
- Contributor submission + review workflow
