---
title: Propriedade Document.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abb766f7a47cbacaededf65eb2b5e9145bf88c60
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698376"
---
# <a name="documentlastupdated-property-dao"></a>Propriedade Document.LastUpdated (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Retorna a data e a hora da alteração feita mais recentemente em um objeto. **Variant** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . LastUpdated

*expressão* Uma variável que representa um objeto **Document** .

## <a name="remarks"></a>Comentários

**DateCreated** e **LastUpdated** retornam a data e a hora em que o objeto foi criado ou atualizado pela última vez. Em um ambiente de vários usuários, os usuários devem obter essas configurações diretamente do servidor de arquivos para evitar discrepâncias nas configurações das propriedades DateCreated e LastUpdated.

