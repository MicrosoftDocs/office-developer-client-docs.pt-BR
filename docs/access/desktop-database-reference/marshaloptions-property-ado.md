---
title: Propriedade MarshalOptions (ADO)
TOCTitle: MarshalOptions Property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f290f2f4fb4820fb01d3a63aef7bcfbfa7c1f035
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464514"
---
# <a name="marshaloptions-property-ado"></a>Propriedade MarshalOptions (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica quais registros serão empacotados de volta para o servidor.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor [MarshalOptionsEnum](marshaloptionsenum.md). O valor padrão é **adMarshalAll**.

## <a name="remarks"></a>Comentários

Ao usar um [Recordset](recordset-object-ado.md) do lado do cliente, os registros que foram modificados no cliente são gravados de volta na camada intermediária ou no servidor Web por meio de uma técnica chamada empacotamento, o processo de empacotar e enviar parâmetros de método de interface através de limites do encadeamento ou do processo. Definir a propriedade **MarshalOptions** pode melhorar o desempenho quando dados remotos modificados são empacotados para atualização de volta à camada intermediária ou ao servidor Web.

**Uso de serviço de dados remotos** Essa propriedade é usada somente em um **Recordset**do lado do cliente.

