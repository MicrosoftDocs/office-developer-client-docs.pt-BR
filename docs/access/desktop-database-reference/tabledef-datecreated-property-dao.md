---
title: Propriedade TableDef.DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2cf97df5d5861a3bb0fdac34ceabc8f732a87d5c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885595"
---
# <a name="tabledefdatecreated-property-dao"></a>Propriedade TableDef.DateCreated (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Retorna a hora e a data nas quais um objeto foi criado (somente em espaços de trabalho do Microsoft Access). **Variant** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . DateCreated

*expressão* Uma variável que representa um objeto **TableDef** .

## <a name="remarks"></a>Comentários

**DateCreated** e **LastUpdated** retornam a data e a hora em que o objeto foi criado ou atualizado pela última vez. Em um ambiente de vários usuários, os usuários devem obter essas configurações diretamente do servidor de arquivos para evitar discrepâncias nas configurações das propriedades DateCreated e LastUpdated.

