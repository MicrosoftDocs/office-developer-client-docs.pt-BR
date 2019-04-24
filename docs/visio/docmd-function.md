---
title: Função DOCMD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60100
localization_priority: Normal
ms.assetid: 6574edeb-eb6f-afd9-89c4-eb5996dffa30
description: Executa o comando identificado.
ms.openlocfilehash: 9e5c02c9a90f3aab66c5d582c83d7d9d892f964c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315229"
---
# <a name="docmd-function"></a><span data-ttu-id="bd7ce-103">Função DOCMD</span><span class="sxs-lookup"><span data-stu-id="bd7ce-103">DOCMD Function</span></span>

<span data-ttu-id="bd7ce-104">Executa o comando identificado.</span><span class="sxs-lookup"><span data-stu-id="bd7ce-104">Performs the identified command.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="bd7ce-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd7ce-105">Syntax</span></span>

 <span data-ttu-id="bd7ce-106">**DoCmd** ( _commandID_)</span><span class="sxs-lookup"><span data-stu-id="bd7ce-106">**DOCMD**( _commandID_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="bd7ce-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd7ce-107">Parameters</span></span>

|<span data-ttu-id="bd7ce-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="bd7ce-108">**Name**</span></span>|<span data-ttu-id="bd7ce-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="bd7ce-109">**Required/Optional**</span></span>|<span data-ttu-id="bd7ce-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="bd7ce-110">**Data Type**</span></span>|<span data-ttu-id="bd7ce-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bd7ce-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bd7ce-112">_commandID_</span><span class="sxs-lookup"><span data-stu-id="bd7ce-112">_commandID_</span></span> <br/> |<span data-ttu-id="bd7ce-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="bd7ce-113">Required</span></span>  <br/> |<span data-ttu-id="bd7ce-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="bd7ce-114">**Number**</span></span> <br/> | <span data-ttu-id="bd7ce-115">O comando a ser executado.</span><span class="sxs-lookup"><span data-stu-id="bd7ce-115">The command to perform.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd7ce-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd7ce-116">Remarks</span></span>

<span data-ttu-id="bd7ce-117">Para obter uma lista de comandos que são compatíveis com a função DOCMD, consulte o tópico "comandos DoCmd/DOCMD" na referência de automação do Microsoft Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="bd7ce-117">For a list of commands that are supported with the DOCMD function, see the topic "DoCmd/DOCMD commands" in the Microsoft Visio 2013 Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="bd7ce-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bd7ce-118">Example</span></span>

 `DOCMD (1312)`
  
<span data-ttu-id="bd7ce-119">Faz com que a caixa de diálogo **Dados da Forma** seja exibida na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="bd7ce-119">Causes the **Shape Data** dialog box to appear in the user interface.</span></span> 
  

