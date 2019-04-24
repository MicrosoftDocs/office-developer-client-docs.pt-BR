---
title: Propriedade DBEngine. defaultType (DAO)
TOCTitle: DefaultType Property
ms:assetid: b4371f3e-1ce0-1d0f-93a8-0c5329b510ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822060(v=office.15)
ms:contentKeyID: 48547217
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053580
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 23f6c87ede6da2cc5b2f3203bfa13cb17bf93e82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294376"
---
# <a name="dbenginedefaulttype-property-dao"></a>Propriedade DBEngine. defaultType (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna um valor que indica o tipo de espaço de trabalho que será utilizado pelo próximo objeto **[Workspace](workspace-object-dao.md)** criado.

## <a name="syntax"></a>Sintaxe

*expressão* . DefaultType

*expressão* Uma variável que representa um objeto **DBEngine** .

## <a name="remarks"></a>Comentários

A configuração ou o valor de retorno pode ser uma das constantes **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)**.


> [!NOTE]
> [!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.

A configuração pode ser substituída por um único **espaço de trabalho** , definindo o argumento Type para o método CreateWorkspace. **[](dbengine-createworkspace-method-dao.md)**

