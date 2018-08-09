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
ms.openlocfilehash: e425dd9605c18d4647787c5df7aeaa4fd5f9e4cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771737"
---
# <a name="docmd-function"></a><span data-ttu-id="1321e-103">Função DOCMD</span><span class="sxs-lookup"><span data-stu-id="1321e-103">DOCMD Function</span></span>

<span data-ttu-id="1321e-104">Executa o comando identificado.</span><span class="sxs-lookup"><span data-stu-id="1321e-104">Performs the identified command.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1321e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1321e-105">Syntax</span></span>

 <span data-ttu-id="1321e-106">**DOCMD** ( _ID de comando_)</span><span class="sxs-lookup"><span data-stu-id="1321e-106">**DOCMD**( _commandID_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="1321e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1321e-107">Parameters</span></span>

|<span data-ttu-id="1321e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="1321e-108">**Name**</span></span>|<span data-ttu-id="1321e-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="1321e-109">**Required/Optional**</span></span>|<span data-ttu-id="1321e-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="1321e-110">**Data Type**</span></span>|<span data-ttu-id="1321e-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1321e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1321e-112">_ID de comando_</span><span class="sxs-lookup"><span data-stu-id="1321e-112">_commandID_</span></span> <br/> |<span data-ttu-id="1321e-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1321e-113">Required</span></span>  <br/> |<span data-ttu-id="1321e-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="1321e-114">**Number**</span></span> <br/> | <span data-ttu-id="1321e-115">O comando a ser executado.</span><span class="sxs-lookup"><span data-stu-id="1321e-115">The command to perform.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1321e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1321e-116">Remarks</span></span>

<span data-ttu-id="1321e-117">Para obter uma lista de comandos que são compatíveis com a função DOCMD, consulte o tópico "Comandos DoCmd/DOCMD" na referência de automação do Microsoft Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="1321e-117">For a list of commands that are supported with the DOCMD function, see the topic "DoCmd/DOCMD commands" in the Microsoft Visio 2013 Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="1321e-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1321e-118">Example</span></span>

 `DOCMD (1312)`
  
<span data-ttu-id="1321e-119">Faz com que a caixa de diálogo **Dados da Forma** seja exibida na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1321e-119">Causes the **Shape Data** dialog box to appear in the user interface.</span></span> 
  

