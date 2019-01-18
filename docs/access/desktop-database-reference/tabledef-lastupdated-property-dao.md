---
title: Propriedade TableDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 994543132fb5323566bd876da066419d0986bd91
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722771"
---
# <a name="tabledeflastupdated-property-dao"></a>Propriedade TableDef.LastUpdated (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Retorna a data e a hora da alteração feita mais recentemente em um objeto. **Variant** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . LastUpdated

*expressão* Uma variável que representa um objeto **TableDef** .

## <a name="remarks"></a>Comentários

**DateCreated** e **LastUpdated** retornam a data e a hora em que o objeto foi criado ou atualizado pela última vez. Em um ambiente de vários usuários, os usuários devem obter essas configurações diretamente do servidor de arquivos para evitar discrepâncias nas configurações das propriedades DateCreated e LastUpdated.

