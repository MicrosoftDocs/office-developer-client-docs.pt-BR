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
# <a name="dbenginedefaulttype-property-dao"></a><span data-ttu-id="fffcd-102">Propriedade DBEngine.DefaultType (DAO)</span><span class="sxs-lookup"><span data-stu-id="fffcd-102">DBEngine.DefaultType Property (DAO)</span></span>


<span data-ttu-id="fffcd-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="fffcd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fffcd-104">Define ou retorna um valor que indica o tipo de espaço de trabalho que será utilizado pelo próximo objeto **[Workspace](workspace-object-dao.md)** criado.</span><span class="sxs-lookup"><span data-stu-id="fffcd-104">Sets or returns a value that indicates what type of workspace will be used by the next **[Workspace](workspace-object-dao.md)** object created.</span></span>

## <a name="syntax"></a><span data-ttu-id="fffcd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fffcd-105">Syntax</span></span>

<span data-ttu-id="fffcd-106">*expressão* . DefaultType</span><span class="sxs-lookup"><span data-stu-id="fffcd-106">*expression* .DefaultType</span></span>

<span data-ttu-id="fffcd-107">*expressão* Uma variável que representa um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="fffcd-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fffcd-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="fffcd-108">Remarks</span></span>

<span data-ttu-id="fffcd-109">A configuração ou o valor de retorno pode ser uma das constantes **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="fffcd-109">The setting or return value can be one of the of the **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** constants.</span></span>


> [!NOTE]
> <span data-ttu-id="fffcd-p101">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="fffcd-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="fffcd-112">A configuração pode ser substituída por um único **Workspace** , definindo o argumento type para o método **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="fffcd-112">The setting can be overridden for a single **Workspace** by setting the type argument to the **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** method.</span></span>

