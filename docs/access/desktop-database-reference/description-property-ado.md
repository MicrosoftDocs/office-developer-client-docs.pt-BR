---
title: Propriedade Description (ADO)
TOCTitle: Description property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba6d05aa1bfb626520af60a30279983bae6fa566
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293928"
---
# <a name="description-property-ado"></a>Propriedade Description (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Descreve um objeto [Error](error-object-ado.md).

## <a name="return-value"></a>Valor de retorno

Retorna um valor **String** contendo uma descrição do erro.

## <a name="remarks"></a>Comentários

Use a propriedade **Description** para obter uma breve descrição do erro. Exiba essa propriedade para alertar o usuário sobre um erro que você não pode ou não deseja resolver. A sequência virá do ADO ou de um provedor.

Os provedores são responsáveis por passar textos de erro específicos para o ADO. O ADO adiciona um objeto [Error](error-object-ado.md) à coleção **Errors** a cada erro de provedor ou alerta que recebe. Enumere a coleção **Errors** para rastrear os erros que são passados pelo provedor.

