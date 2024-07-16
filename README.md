# MarketDataAPI

Access Alpaca’s historical and real-time US stock market and crypto data through REST API and WebSocket. There are APIs for Stock Pricing, Crypto Pricing, and News.

## Building

To install the required dependencies and to build the elixir project, run:

```console
mix local.hex --force
mix do deps.get, compile
```

## Installation

If [available in Hex][], the package can be installed by adding `alpaca_market_data_api` to
your list of dependencies in `mix.exs`:

```elixir
def deps do
  [{:alpaca_market_data_api, "~> 2.0.0"}]
end
```

Documentation can be generated with [ExDoc][] and published on [HexDocs][]. Once published, the docs can be found at
[https://hexdocs.pm/alpaca_market_data_api][docs].

## Configuration

You can override the URL of your server (e.g. if you have a separate development and production server in your
configuration files).

```elixir
config :alpaca_market_data_api, base_url: "https://data.alpaca.markets"
```

Multiple clients for the same API with different URLs can be created passing different `base_url`s when calling
`MarketDataAPI.Connection.new/1`:

```elixir
client = MarketDataAPI.Connection.new(base_url: "https://data.alpaca.markets")
```

[exdoc]: https://github.com/elixir-lang/ex_doc
[hexdocs]: https://hexdocs.pm
[available in hex]: https://hex.pm/docs/publish
[docs]: https://hexdocs.pm/alpaca_market_data_api
