# Acceptance criteria US-001

Skill: A2.04. Template: `.github/sdlc/templates/acceptance-criteria.md`. Source ID: T-01 (docs/sdlc/inputs/T-01/story.md, line 5).

- Criterion ID: AC-001
  - Given: the shopper is on a product's product page
  - When: the shopper adds the product to the cart
  - Then (one observable result): the product is in the shopper's cart
  - Platform difference: none stated
  - Source: T-01 line 5 ("add a product to my cart from its product page")

- Criterion ID: AC-002
  - Given: a product was added to the cart
  - When: the shopper comes back later
  - Then (one observable result): the product is still in the cart
  - Platform difference: none stated
  - Source: T-01 line 5 ("so that I can buy it later"); how long "later" lasts is TBD

- Criterion ID: AC-003
  - Given: the shopper is on a product's product page
  - When: the shopper adds the product to the cart
  - Then (one observable result): TBD (the source does not state what the shopper sees after adding)
  - Platform difference: none stated
  - Source: T-01 line 5; result not stated

## Checkpoints raised
- TBD AC-002 duration of "later" → docs/sdlc/checkpoints/CP-07-cart-later.md
- TBD AC-003 feedback after adding → docs/sdlc/checkpoints/CP-07-add-to-cart-feedback.md
