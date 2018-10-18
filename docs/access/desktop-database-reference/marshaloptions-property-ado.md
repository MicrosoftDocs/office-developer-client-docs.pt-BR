---
<<<<<<< Título cabeça: propriedade MarshalOptions (ADO) TOCTitle: propriedade MarshalOptions (ADO) === título: propriedade MarshalOptions (ADO) TOCTitle: propriedade MarshalOptions (ADO)
>>>>>>> ms:assetid de mestre: dc9c4e94-0725-210d-8251-079054541142 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15) ms:contentKeyID: ms.date 48548143: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="marshaloptions-property-ado"></a>Propriedade MarshalOptions (ADO)
=======
# <a name="marshaloptions-property-ado"></a>Propriedade MarshalOptions (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica quais registros serão empacotados de volta para o servidor.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor [MarshalOptionsEnum](marshaloptionsenum.md). O valor padrão é **adMarshalAll**.

## <a name="remarks"></a>Comentários

<<<<<<< Cabeça ao usar um [Recordset](recordset-object-ado.md)do lado do cliente, os registros que foram modificados no cliente são gravados na camada intermediária ou o servidor Web por meio de uma técnica chamada marshaling, o processo de empacotamento e envio de interface parâmetros de método entre limites de thread ou processo. Definir a propriedade **MarshalOptions** pode melhorar o desempenho quando dados remotos modificados são empacotados para atualização de volta à camada intermediária ou ao servidor Web.
=== Quando estiver usando um [Recordset](recordset-object-ado.md)do lado do cliente, os registros que foram modificados no cliente são gravados na camada intermediária ou um servidor web por meio de uma técnica chamada marshaling, o processo de empacotamento e envio de parâmetros de método de interface entre limites do processo ou segmento. A configuração da propriedade **MarshalOptions** pode melhorar o desempenho quando é empacotados de dados remotos modificados para a atualização de volta para o servidor web ou camada intermediária.
>>>>>>> mestre

**Uso de serviço de dados remotos** Essa propriedade é usada somente em um **Recordset**do lado do cliente.

