# Example: ticket → scaffold

## Ticket (self-generated)
Add `GET /recipes/:id/nutrition` — return computed nutrition totals for
a recipe based on its ingredient list.

## Analyst summary
- Closest pattern: `GET /recipes/:id` (controller → service → repo → DTO)
- Repo layer: `RecipeRepository.findById`
- DTO convention: plain object, camelCase, in `dto/RecipeDTO.ts`

## Scaffold output (beginner density)

```ts
// controllers/nutritionController.ts
export async function getNutrition(req, res) {
  // TODO: get recipeId from req.params
  // TODO: call nutritionService.computeForRecipe(recipeId)
  // TODO: if not found, return 404
  // TODO: send result as JSON
}

// services/nutritionService.ts
export async function computeForRecipe(recipeId: string) {
  // TODO: fetch recipe + ingredients via RecipeRepository
  // TODO: sum calories/protein/fat across ingredients
  // TODO: map to NutritionDTO shape (see dto/RecipeDTO.ts for style)
}
```

No implementation given — fill in each TODO, then ask for a review pass.
