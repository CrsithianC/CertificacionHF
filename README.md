1 1er Error: cambiar el nombre del archivo TLS en - ORDERER_ADMIN_TLS_CERTIFICATE de servre.crt a server.crt
  2do Error: en la ruta de los certificados hyperledger esta mal escrito
2 1er Error: Al chaincode le faltaba una '}' en la función CreateAsset
2 2do Error: dar permisos al script de createChannel para que se genere y las Orgs puedan comunicarse
3 Logs : Añadir logging:
      format: json
      level: info
      en el archivo .yaml de la configuracion de los peers y orderers
  Añadir logging:
      level: debug
      modules:
        gossip: warning
        chaincode: info
      format '%{msg} %{time}'
en core.yaml
