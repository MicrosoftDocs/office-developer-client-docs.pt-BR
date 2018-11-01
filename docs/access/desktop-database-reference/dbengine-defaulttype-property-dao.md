---
title: Propriedade DBEngine.DefaultType (DAO)
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
ms.openlocfilehash: f0fa2fb5ba12b1537994a4d6df88406db38bfec4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870919"
---
# <a name="dbenginedefaulttype-property-dao"></a>Propriedade DBEngine.DefaultType (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna um valor que indica o tipo de espaço de trabalho que será utilizado pelo próximo objeto **[Workspace](workspace-object-dao.md)** criado.

## <a name="syntax"></a>Sintaxe

*expressão* . DefaultType

*expressão* Uma variável que representa um objeto **DBEngine** .

## <a name="remarks"></a>Comentários

A configuração ou o valor de retorno pode ser uma das constantes **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)**.


> [!NOTE]
> [!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.

A configuração pode ser substituída por um único **Workspace** , definindo o argumento type para o método **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** .

