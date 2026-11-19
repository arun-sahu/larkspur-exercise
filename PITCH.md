# PITCH.md

Six lines and a lever. Your words. The last two are scored.

Built: A support agent for disrupted flights, offered eleven tools: Larkspur's nine, our own next_available_day, and fare_rules over MCP.
Does: For a customer whose flight was cancelled (K7PQ2M, LK415 Denver to Austin, weather), it finds the booking, checks the flight status, applies the cancellation policy, and lists the alternative flights with seats left.
Number: 61,706 to 64,120 tokens in, total of the five tickets.
Safety check: It looked things up and explained options but did not hold or book a seat by itself; the K7PQ2M trace has four read-only calls and no hold_seat or confirm_rebooking.
Next: Pass the party size into the seat search, so the agent can answer whether there is room for everyone travelling.
Still broken: When a customer asks for room for three, the agent cannot check for three seats: search_alternatives was called with only the PNR, and next_available_day answers for one passenger.
Lever: cost

## Priya asked

Costs:
Wrong:
Runs it:
Left out:
