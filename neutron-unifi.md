# Migration

```go

type DevicePortOverrides struct {
	AggregateNumPorts            int               `json:"aggregate_num_ports,omitempty"` // [1-8]
	Autoneg                      *bool             `json:"autoneg,omitempty"`
	Dot1XCtrl                    string            `json:"dot1x_ctrl,omitempty"`             // auto|force_authorized|force_unauthorized|mac_based|multi_host
	Dot1XIDleTimeout             int               `json:"dot1x_idle_timeout,omitempty"`     // [0-9]|[1-9][0-9]{1,3}|[1-5][0-9]{4}|6[0-4][0-9]{3}|65[0-4][0-9]{2}|655[0-2][0-9]|6553[0-5]
	EgressRateLimitKbps          int               `json:"egress_rate_limit_kbps,omitempty"` // 6[4-9]|[7-9][0-9]|[1-9][0-9]{2,6}
	EgressRateLimitKbpsEnabled   *bool             `json:"egress_rate_limit_kbps_enabled,omitempty"`
	ExcludedNetworkIDs           []string          `json:"excluded_networkconf_ids,omitempty"`
	FecMode                      string            `json:"fec_mode,omitempty"` // rs-fec|fc-fec|default|disabled
	Forward                      string            `json:"forward,omitempty"`  // all|native|customize|disabled
	FullDuplex                   *bool             `json:"full_duplex,omitempty"`
	Isolation                    *bool             `json:"isolation,omitempty"`
	LldpmedEnabled               *bool             `json:"lldpmed_enabled,omitempty"`
	LldpmedNotifyEnabled         *bool             `json:"lldpmed_notify_enabled,omitempty"`
	MirrorPortIDX                int               `json:"mirror_port_idx,omitempty"` // [1-9]|[1-4][0-9]|5[0-2]
	NATiveNetworkID              string            `json:"native_networkconf_id,omitempty"`
	Name                         string            `json:"name,omitempty"`     // .{0,128}
	OpMode                       string            `json:"op_mode,omitempty"`  // switch|mirror|aggregate
	PoeMode                      string            `json:"poe_mode,omitempty"` // auto|pasv24|passthrough|off
	PortIDX                      int               `json:"port_idx,omitempty"` // [1-9]|[1-4][0-9]|5[0-2]
	PortKeepaliveEnabled         *bool             `json:"port_keepalive_enabled,omitempty"`
	PortProfileID                string            `json:"portconf_id,omitempty"` // [\d\w]+
	PortSecurityEnabled          *bool             `json:"port_security_enabled,omitempty"`
	PortSecurityMACAddress       []string          `json:"port_security_mac_address,omitempty"` // ^([0-9A-Fa-f]{2}[:]){5}([0-9A-Fa-f]{2})$
	PriorityQueue1Level          int               `json:"priority_queue1_level,omitempty"`     // [0-9]|[1-9][0-9]|100
	PriorityQueue2Level          int               `json:"priority_queue2_level,omitempty"`     // [0-9]|[1-9][0-9]|100
	PriorityQueue3Level          int               `json:"priority_queue3_level,omitempty"`     // [0-9]|[1-9][0-9]|100
	PriorityQueue4Level          int               `json:"priority_queue4_level,omitempty"`     // [0-9]|[1-9][0-9]|100
	QOSProfile                   *DeviceQOSProfile `json:"qos_profile,omitempty"`
	SettingPreference            string            `json:"setting_preference,omitempty"` // auto|manual
	Speed                        int               `json:"speed,omitempty"`              // 10|100|1000|2500|5000|10000|20000|25000|40000|50000|100000
	StormctrlBroadcastastEnabled *bool             `json:"stormctrl_bcast_enabled,omitempty"`
	StormctrlBroadcastastLevel   int               `json:"stormctrl_bcast_level,omitempty"` // [0-9]|[1-9][0-9]|100
	StormctrlBroadcastastRate    int               `json:"stormctrl_bcast_rate,omitempty"`  // [0-9]|[1-9][0-9]{1,6}|1[0-3][0-9]{6}|14[0-7][0-9]{5}|148[0-7][0-9]{4}|14880000
	StormctrlMcastEnabled        *bool             `json:"stormctrl_mcast_enabled,omitempty"`
	StormctrlMcastLevel          int               `json:"stormctrl_mcast_level,omitempty"` // [0-9]|[1-9][0-9]|100
	StormctrlMcastRate           int               `json:"stormctrl_mcast_rate,omitempty"`  // [0-9]|[1-9][0-9]{1,6}|1[0-3][0-9]{6}|14[0-7][0-9]{5}|148[0-7][0-9]{4}|14880000
	StormctrlType                string            `json:"stormctrl_type,omitempty"`        // level|rate
	StormctrlUcastEnabled        *bool             `json:"stormctrl_ucast_enabled,omitempty"`
	StormctrlUcastLevel          int               `json:"stormctrl_ucast_level,omitempty"` // [0-9]|[1-9][0-9]|100
	StormctrlUcastRate           int               `json:"stormctrl_ucast_rate,omitempty"`  // [0-9]|[1-9][0-9]{1,6}|1[0-3][0-9]{6}|14[0-7][0-9]{5}|148[0-7][0-9]{4}|14880000
	StpPortMode                  *bool             `json:"stp_port_mode,omitempty"`
	TaggedVLANMgmt               string            `json:"tagged_vlan_mgmt,omitempty"` // auto|block_all|custom
	VoiceNetworkID               string            `json:"voice_networkconf_id,omitempty"`

	PortPoe *bool `json:"port_poe,omitempty"`
}
```