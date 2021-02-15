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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308411"
---
# <a name="tabledeflastupdated-property-dao"></a>Propriedade TableDef.LastUpdated (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Retorna a data e a hora da alteração mais recente feita em um objeto. **Variant** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . LastUpdated

*expressão* Uma variável que representa um objeto **TableDef**.

## <a name="remarks"></a>Comentários

**DateCreated** e **LastUpdated** retornam a data e a hora nas quais o objeto foi criado ou atualizado pela última vez. Em um ambiente multiusuário, os usuários devem obter essas definições diretamente do servidor de arquivos para evitar discrepâncias nas definições das propriedades DateCreated e LastUpdated.

