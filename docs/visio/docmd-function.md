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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413070"
---
# <a name="docmd-function"></a><span data-ttu-id="901e6-103">Função DOCMD</span><span class="sxs-lookup"><span data-stu-id="901e6-103">DOCMD Function</span></span>

<span data-ttu-id="901e6-104">Executa o comando identificado.</span><span class="sxs-lookup"><span data-stu-id="901e6-104">Performs the identified command.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="901e6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="901e6-105">Syntax</span></span>

 <span data-ttu-id="901e6-106">**DoCmd** ( _commandID_)</span><span class="sxs-lookup"><span data-stu-id="901e6-106">**DOCMD**( _commandID_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="901e6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="901e6-107">Parameters</span></span>

|<span data-ttu-id="901e6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="901e6-108">**Name**</span></span>|<span data-ttu-id="901e6-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="901e6-109">**Required/Optional**</span></span>|<span data-ttu-id="901e6-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="901e6-110">**Data Type**</span></span>|<span data-ttu-id="901e6-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="901e6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="901e6-112">_commandID_</span><span class="sxs-lookup"><span data-stu-id="901e6-112">_commandID_</span></span> <br/> |<span data-ttu-id="901e6-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="901e6-113">Required</span></span>  <br/> |<span data-ttu-id="901e6-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="901e6-114">**Number**</span></span> <br/> | <span data-ttu-id="901e6-115">O comando a ser executado.</span><span class="sxs-lookup"><span data-stu-id="901e6-115">The command to perform.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="901e6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="901e6-116">Remarks</span></span>

<span data-ttu-id="901e6-117">Para obter uma lista de comandos que são compatíveis com a função DOCMD, consulte o tópico "comandos DoCmd/DOCMD" na referência de automação do Microsoft Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="901e6-117">For a list of commands that are supported with the DOCMD function, see the topic "DoCmd/DOCMD commands" in the Microsoft Visio 2013 Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="901e6-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="901e6-118">Example</span></span>

 `DOCMD (1312)`
  
<span data-ttu-id="901e6-119">Faz com que a caixa de diálogo **Dados da Forma** seja exibida na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="901e6-119">Causes the **Shape Data** dialog box to appear in the user interface.</span></span> 
  

