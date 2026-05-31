1. Take a ticket/input.
2. Ask your preferred model to extract claims as JSON.
3. Send that JSON into Aurora.
4. Aurora checks contradictions, policy, risk, and confidence.
5. Aurora returns a decision + audit trail.

ticket = load_ticket("ticket.json")

prompt = make_extraction_prompt(ticket)

model_output = your_model.generate(prompt)

claims_json = repair_or_validate_json(model_output)

result = aurora_runtime.run(
    ticket=ticket,
    external_claims=claims_json["claims"],
    forced_router_mode=claims_json.get("suggested_router_mode")
)

print(result["decision"])
print(result["confidence"])
print(result["audit_log"])


Your model does the language part.
Aurora does the consistency-checking part.
