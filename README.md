
<body>
  <h1>wots.live – API Documentation</h1>
  <p><strong>Website:</strong> <a href="https://wots.live" target="_blank">https://wots.live</a></p>

  <p>This document provides an overview of the APIs and WebSocket endpoint used in the <strong>wots.live</strong> streaming interface.</p>

  <h2>1. Supabase Channels Lookup</h2>
  <p>
    <code>GET https://jcbvjakdtywqikciddqq.supabase.co/rest/v1/channels?select=*&name=ilike.{username}</code>
  </p>
  <p><strong>Description:</strong> Lookup channel data by username (partial or full match).</p>
  <p><strong>Note:</strong> Requires API Key via header or query string.</p>
  <pre>
Headers:
  apikey: YOUR_SUPABASE_API_KEY
  Authorization: Bearer YOUR_SUPABASE_API_KEY
  </pre>

  <h2>2. Get Livestream Info</h2>
  <p>
    <code>GET https://api.livebeam.live/api/get_livestream?channel_id={streamer_id}</code><br>
     <code>GET https://api.livebeam.live/api/get-livestreams?channel_id={streamer_id}&page=1&limit=2</code>
  </p>
  <p><strong>Description:</strong> Retrieve current livestream information for a specific channel.</p>


  <h2>3. Get Follower Count</h2>
  <p>
    <code>GET https://api.livebeam.live/api/follower-count/{streamer_id}</code>
  </p>
  <p><strong>Description:</strong> Returns the total follower count for the given channel.</p>

  <h2>4. Live Chat via WebSocket</h2>
  <p>
    <code>wss://chat.livebeam.live/ws?channel_id={channel_id}&guest=true</code>
  </p>
  <p><strong>Description:</strong> Connect to the live chat websocket for a channel. Guests can read and send messages depending on channel settings.</p>

  <h2>Authentication Notes</h2>
  <p>Some endpoints require authentication or API keys. Ensure you attach proper headers or query parameters where applicable.</p>

  <h2>Disclaimer</h2>
  <p>This is an unofficial API reference based on observed usage by <code>wots.live</code>. Endpoints may change without notice.</p>
