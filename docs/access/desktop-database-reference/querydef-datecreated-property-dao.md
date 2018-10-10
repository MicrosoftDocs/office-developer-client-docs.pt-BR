---
title: Propriedade QueryDef.DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62fcad68a50ac7f2a09675d9ac51734c4147d207
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464915"
---
# <a name="querydefdatecreated-property-dao"></a>Propriedade QueryDef.DateCreated (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Retorna a hora e a data nas quais um objeto foi criado (somente em espaços de trabalho do Microsoft Access). **Variant** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . DateCreated

*expressão* Uma variável que representa um objeto **QueryDef** .

## <a name="remarks"></a>Comentários

**DateCreated** e **LastUpdated** retornam a data e a hora em que o objeto foi criado ou atualizado pela última vez. Em um ambiente de vários usuários, os usuários devem obter essas configurações diretamente do servidor de arquivos para evitar discrepâncias nas configurações das propriedades DateCreated e LastUpdated.

