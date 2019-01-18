---
title: Propriedade MarshalOptions (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 22a3662d3d14dd639069fa7aa48eda6f032fd2d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704592"
---
# <a name="marshaloptions-property-ado"></a>Propriedade MarshalOptions (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica quais registros serão empacotados de volta para o servidor.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor [MarshalOptionsEnum](marshaloptionsenum.md). O valor padrão é **adMarshalAll**.

## <a name="remarks"></a>Comentários

Ao usar um [Recordset](recordset-object-ado.md)do lado do cliente, os registros que foram modificados no cliente são gravados na camada intermediária ou um servidor web por meio de uma técnica chamada marshaling, o processo de empacotamento e enviar os parâmetros de método de interface através de thread ou limites de processo. A configuração da propriedade **MarshalOptions** pode melhorar o desempenho quando é empacotados de dados remotos modificados para a atualização de volta para o servidor web ou camada intermediária.

**Uso de serviço de dados remotos** Essa propriedade é usada somente em um **Recordset**do lado do cliente.

