---
title: Propriedade DBEngine (DAO)
TOCTitle: Version Property
ms:assetid: b2807dc1-604f-4423-289a-ff38a3d9f31b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822024(v=office.15)
ms:contentKeyID: 48547171
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052986
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1723deea7f29c59fb388a11acc5e5ffcced4abe1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924593"
---
# <a name="dbengineversion-property-dao"></a><span data-ttu-id="6e977-102">Propriedade DBEngine (DAO)</span><span class="sxs-lookup"><span data-stu-id="6e977-102">DBEngine.Version property (DAO)</span></span>


<span data-ttu-id="6e977-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e977-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6e977-p101">Retorna a versão do DAO atualmente em uso. **String** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6e977-p101">Rreturns the version of DAO currently in use. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e977-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e977-106">Syntax</span></span>

<span data-ttu-id="6e977-107">*expressão* . Versão</span><span class="sxs-lookup"><span data-stu-id="6e977-107">*expression* .Version</span></span>

<span data-ttu-id="6e977-108">*expressão* Uma variável que representa um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="6e977-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e977-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e977-109">Remarks</span></span>

<span data-ttu-id="6e977-p102">O valor retornado é uma cadeia de caracteres que avalia um número de versão no formulário "major.minor". Por exemplo, "3.0". O número de versão do produto consiste no número de versão (3), em um ponto e no número de liberação (0).</span><span class="sxs-lookup"><span data-stu-id="6e977-p102">The return value is a String that evaluates to a version number in the form "major.minor". For example, "3.0". The product version number consists of the version number (3), a period, and the release number (0).</span></span>

