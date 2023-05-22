# Simple Calculator

```ruby
simple_calculator_controller = client.simple_calculator
```

## Class Name

`SimpleCalculatorController`


# Get Calculate

Calculates the expression using the specified operation.

```ruby
def get_calculate(options = {})
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `operation` | [`OperationTypeEnum`](../../doc/models/operation-type-enum.md) | Template, Required | The operator to apply on the variables |
| `x` | `Float` | Query, Required | The LHS value |
| `y` | `Float` | Query, Required | The RHS value |

## Response Type

`Float`

## Example Usage

```ruby
collect = {
  'operation': OperationTypeEnum::MULTIPLY,
  'x': 222.14,
  'y': 165.14
}

result = simple_calculator_controller.get_calculate(collect)
```

