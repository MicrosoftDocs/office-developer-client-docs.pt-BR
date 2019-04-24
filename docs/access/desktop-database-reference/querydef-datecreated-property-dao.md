---
title: Propriedade QueryDef. DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4a120eed6c20db73e1c23f31ea9329d00da2f0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301068"
---
# <a name="querydefdatecreated-property-dao"></a>Propriedade QueryDef. DateCreated (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Retorna a hora e a data nas quais um objeto foi criado (somente em espaços de trabalho do Microsoft Access). **Variant** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . DateCreated

*expressão* Uma variável que representa um objeto **QueryDef** .

## <a name="remarks"></a>Comentários

**DateCreated** e **LastUpdated** retornam a data e a hora nas quais o objeto foi criado ou atualizado pela última vez. Em um ambiente multiusuário, os usuários devem obter essas definições diretamente do servidor de arquivos para evitar discrepâncias nas definições das propriedades DateCreated e LastUpdated.

