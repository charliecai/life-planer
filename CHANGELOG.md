# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] - 2025-12-31

### Added
- **Annual Review Template** - Comprehensive 12-section annual retrospective template
  - Pattern recognition (positive feedback, cost patterns, repeated failures)
  - Life Wheel year-end assessment
  - Goal achievement review
  - Time & energy audit
  - Financial, health, and relationship reviews
  - Key insights and action items for next year
- **Smart Pre-Planning Review Check** - Automatically checks if review exists before planning
  - Suggests creating annual review before annual planning
  - Suggests creating monthly review before monthly planning
  - User can choose to do review first or skip directly to planning
- **Time Period Calculation Rules** - Clear rules for calculating years and months
  - Automatic calculation based on current date
  - User override support for any custom time period
  - Examples and edge cases documented
- **Multi-language Support** - Language adapts to user input
  - Default: English
  - Automatically switches to Chinese if user communicates in Chinese
  - Maintains language consistency throughout session

### Changed
- **Annual Plan Template** - Removed annual review section (now separate template)
  - Restructured from 8 sections to 7 sections
  - Updated section numbering
- **SKILL.md** - Enhanced workflow instructions
  - Added time period confirmation as first interaction principle
  - Updated template references to include annual review
  - Added pre-planning review check workflow

### Fixed
- Year calculation logic - Now correctly identifies current year for review and next year for planning
- Month calculation logic - Properly handles current month vs. next month scenarios

## [1.0.0] - 2024-12-30

### Added
- Initial release
- Annual Planning workflow (Phase 0-8)
- Monthly Planning workflow (Phase 9)
- Monthly Review workflow (Phase 10)
- Life Wheel Assessment
- Annual Plan Template
- Monthly Plan Template
- Monthly Review Template
- Basic skill configuration
