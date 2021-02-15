---
title: Método QueryDef.Close (DAO)
TOCTitle: Close Method
ms:assetid: b2b63462-453d-9e2b-0bb3-69a4a7a6ecef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822031(v=office.15)
ms:contentKeyID: 48547179
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052976
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4d50fa52ff4f5d669b062a052bf3e59a28a9e732
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303301"
---
# <a name="querydefclose-method-dao"></a><span data-ttu-id="31142-102">Método QueryDef.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="31142-102">QueryDef.Close method (DAO)</span></span>


<span data-ttu-id="31142-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="31142-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31142-104">Fecha um objeto **QueryDef** aberto.</span><span class="sxs-lookup"><span data-stu-id="31142-104">Closes an open **QueryDef**.</span></span>

## <a name="syntax"></a><span data-ttu-id="31142-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31142-105">Syntax</span></span>

<span data-ttu-id="31142-106">*expressão* .Close</span><span class="sxs-lookup"><span data-stu-id="31142-106">*expression* .Close</span></span>

<span data-ttu-id="31142-107">*expressão* Uma variável que representa um objeto **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="31142-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="31142-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="31142-108">Remarks</span></span>

<span data-ttu-id="31142-109">Se o objeto **QueryDef** já estiver fechado quando você usar **Close**, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="31142-109">If the **QueryDef** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="31142-110">Uma alternativa ao método **Fechar**, é definir o valor de uma variável de um objeto para **Nada** (Definir dbsTemp = Nada).</span><span class="sxs-lookup"><span data-stu-id="31142-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

