---
title: Propriedade Marshaloptions (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 22a3662d3d14dd639069fa7aa48eda6f032fd2d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289767"
---
# <a name="marshaloptions-property-ado"></a>Propriedade Marshaloptions (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica quais registros serão empacotados de volta para o servidor.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor [MarshalOptionsEnum](marshaloptionsenum.md). O valor padrão é **adMarshalAll**.

## <a name="remarks"></a>Comentários

Ao usar um [Recordset](recordset-object-ado.md)do lado do cliente, os registros que foram modificados no cliente são gravados novamente na camada intermediária ou servidor Web por meio de uma técnica chamada marshaling, o processo de empacotamento e envio de parâmetros de método de interface no thread ou limites do processo. A definição **** da propriedade marshaloptions pode melhorar o desempenho quando dados remotos modificados são empacotados para atualização de volta para a camada intermediária ou servidor Web.

**Uso do Remote Data Service** Essa propriedade é usada apenas em um **Recordset**do lado do cliente.

