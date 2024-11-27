# Home Automation Setup with Docker Compose
This repository provides configurations and scripts to set up a home automation system using Docker Compose. It includes services like Homebridge for smart home device integration and Pi-hole for network-wide ad blocking.

## Prerequisites
- **Operating System**: Linux-based system (e.g., Ubuntu)
- **Docker**: Installed and running
- **Docker Compose**: Installed

## Services Included
1. **[Homebridge](https://homebridge.io/)**: Integrates non-HomeKit-compatible devices into Apple’s HomeKit ecosystem.
2. **[Pi-hole](https://pi-hole.net/)**: Provides network-wide ad blocking and enhances privacy.
3. **[RIPE Atlas Probe](https://atlas.ripe.net/)**: Participates in a global network that measures Internet connectivity and reachability, providing real-time data on the state of the Internet. Hosting a probe contributes to the RIPE Atlas network, aiding in comprehensive Internet analysis.

## Setup Instructions
1. Clone the Repository:
	```
	git clone https://github.com/brettdavies/home-automation.git
	cd home-automation
	```
2. Configure Environment Variables:
   - Create a `.env` file in the root directory.
   - Define necessary environment variables, such as `WEBPASSWORD` for Pi-hole and `HOMEBRIDGE_CONFIG_UI_PORT` for Homebridge.
3. Deploy Services:
	```
	docker-compose up -d
	```
4. Access Web Interfaces:
   - **Homebridge UI**: Navigate to http://<your-server-ip>:8581
   - **Pi-hole Admin Console**: Navigate to http://<your-server-ip>/admin

## Customization

### Homebridge:
- Install plugins via the Homebridge UI to support various smart home devices.
- Edit the `config.json` file to configure accessories and platforms.

### Pi-hole:
- Update blocklists and whitelist/blacklist domains through the admin console.
- Configure DNS settings as per your network requirements.

## Maintenance
- Updating Services:
- Pull the latest images and recreate containers:
	```
	docker-compose pull
	docker-compose up -d
	```
- Logs and Monitoring:
- View logs for troubleshooting:
	```
	docker-compose logs -f
	```

## Contributing
Contributions are welcome. Please fork the repository and submit a pull request with your enhancements.

# 
*Note: Ensure that your network configuration allows access to the specified ports and that Docker is properly installed and configured on your system.*
