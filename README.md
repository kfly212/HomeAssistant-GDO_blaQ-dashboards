# Garage Door Card
# ----------------
# Home Assistant dashboard card (custom:button-card) for the GDO blaQ garage
# door opener (cover.garage_gdo_blaq_799094_garage_door).
#
# Layout: dark rounded card, with an animated SVG garage on the left and the
# controls on the right.
#   - light:  small round toggle (top-left corner) for switch.garage_lights.
#             Glows yellow when on. Hold for more-info.
#   - img:    SVG of the garage whose door slats move with current_position.
#             Shown greyed out when the door is unavailable/unknown.
#   - label:  "GARAGE DOOR" heading.
#   - state:  big status text (Open / Closed / Opening… / Closing…) and the
#             "% open" value, or "Unavailable".
#   - btn:    action button that runs cover.toggle. Its label changes with the
#             state (Open / Close / Stop). Disabled ("Offline") when unavailable.
#   - slider: range slider that calls cover.set_cover_position on release.
#             Hidden if the entity doesn't report current_position.
#
# The outer card ignores tap/hold/double-tap, so only the inner controls react.
# Requires: button-card (HACS).
