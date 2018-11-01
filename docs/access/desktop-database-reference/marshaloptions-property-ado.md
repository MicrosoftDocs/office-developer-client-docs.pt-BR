---
title: Propriedade MarshalOptions (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f5983b7794677b5cc584c541289069acf282d9f9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883208"
---
# <a name="marshaloptions-property-ado"></a>Propriedade MarshalOptions (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica quais registros serão empacotados de volta para o servidor.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor [MarshalOptionsEnum](marshaloptionsenum.md). O valor padrão é **adMarshalAll**.

## <a name="remarks"></a>Comentários

Ao usar um [Recordset](recordset-object-ado.md)do lado do cliente, os registros que foram modificados no cliente são gravados na camada intermediária ou um servidor web por meio de uma técnica chamada marshaling, o processo de empacotamento e enviar os parâmetros de método de interface através de thread ou limites de processo. A configuração da propriedade **MarshalOptions** pode melhorar o desempenho quando é empacotados de dados remotos modificados para a atualização de volta para o servidor web ou camada intermediária.

**Uso de serviço de dados remotos** Essa propriedade é usada somente em um **Recordset**do lado do cliente.

