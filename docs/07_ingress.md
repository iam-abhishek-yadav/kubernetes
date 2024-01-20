# `Why Ingress?`

## `Enterprise and TLS Load Balancing Capabilities`

### `Sticky Sessions`
- Ingress controllers provide features such as sticky sessions, allowing users to maintain session persistence.

### `TLS Termination`
- Ingress controllers handle TLS termination, enabling secure communication between clients and the backend services.

### `Path-Based Routing`
- Ingress controllers support path-based routing, directing traffic to different services based on the request path.

### `Host-Based Routing`
- Ingress controllers can route traffic based on the host header, allowing multiple services to share the same IP address but respond to different hostnames.

### `Ratio-Based Routing`
- Some Ingress controllers support ratio-based routing, allowing you to distribute traffic based on defined ratios.

## `Load Balancer Considerations`

### `Cloud Charges`
- Using native cloud Load Balancers may incur charges. In contrast, Ingress controllers can be more cost-effective in some scenarios.

## `Ingress Controller Options`

Users can deploy Ingress controllers from various providers like following:

- Nginx
- F5
- Ambassador

## `Host-Based Routing`

- Ingress controllers allow routing based on the host header, enabling the hosting of multiple services on the same IP address but responding to different hostnames.

In summary, Ingress provides a flexible and feature-rich way to manage external access to services in a Kubernetes cluster, offering advantages over native Load Balancer solutions in terms of cost, flexibility, and features.

![Ingress](https://kubernetes.io/docs/images/ingress.svg)

