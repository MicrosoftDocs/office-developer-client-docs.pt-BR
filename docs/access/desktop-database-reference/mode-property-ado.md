---
<<<<<<< Título cabeça: modo Property (ADO) TOCTitle: modo Property (ADO) === título: a propriedade Mode (ADO) TOCTitle: a propriedade Mode (ADO)
>>>>>>> ms:assetid de mestre: 62086f4f-8624-16c4-dae1-a17475d1864d ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15) ms:contentKeyID: ms.date 48545227: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="mode-property-ado"></a>Propriedade Mode (ADO)
=======
# <a name="mode-property-ado"></a>Propriedade Mode (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica as permissões disponíveis para modificar os dados em um objeto [Connection](connection-object-ado.md), [Record](record-object-ado.md) ou [Stream](stream-object-ado.md).

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor [ConnectModeEnum](connectmodeenum.md). O valor padrão para um objeto **Connection** é **adModeUnknown**. O valor padrão para um objeto **Record** é **adModeRead**. O valor padrão para um **Stream** associado a uma fonte de base (aberta com uma URL como a fonte ou como o padrão **Stream** de um **Record**) é **adModeRead**. O valor padrão para um objeto **Stream** não associado a uma fonte de base (instanciada na memória) é **adModeUnknown**.

## <a name="remarks"></a>Comentários

Use a propriedade **Mode** para definir ou retornar as permissões de acesso em uso pelo provedor na conexão atual. Você pode definir a propriedade **Mode** apenas quando o objeto **Connection** estiver fechado.

Para um objeto **Stream**, se o modo de acesso não for especificado, ele será herdado da fonte usada para abrir o objeto **Stream**. Por exemplo, se um **Stream** for aberto a partir de um objeto **Record**, por padrão, ele será aberto no mesmo modo que o **Record**.

Esta propriedade será leitura/gravação enquanto o objeto estiver fechado e somente leitura quando estiver aberto.

**Uso de serviço de dados remotos** Quando usado em um objeto de Conexão do cliente, a propriedade **Mode** só pode ser definida como **adModeUnknown**.

