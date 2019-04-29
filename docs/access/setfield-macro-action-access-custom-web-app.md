---
title: Ação de macro SetField (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: A ação DefinirCampo pode ser usada para atribuir um valor a um campo.
ms.openlocfilehash: c67c66c238b68512aec90cf6d82d7d497e16ecf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432923"
---
# <a name="setfield-macro-action-access-custom-web-app"></a><span data-ttu-id="52e22-103">Ação de macro SetField (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="52e22-103">SetField Macro Action (Access custom web app)</span></span>

<span data-ttu-id="52e22-104">A ação **DefinirCampo** pode ser usada para atribuir um valor a um campo.</span><span class="sxs-lookup"><span data-stu-id="52e22-104">The **SetField** action can be used to assign a value to a field.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="52e22-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="52e22-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="52e22-107">A ação **DefinirCampo** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="52e22-107">The **SetField** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="52e22-108">Setting</span><span class="sxs-lookup"><span data-stu-id="52e22-108">Setting</span></span>

<span data-ttu-id="52e22-109">A ação **DefinirCampo** tem os seguintes listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="52e22-109">The **SetField** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="52e22-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="52e22-110">**Argument name**</span></span>|<span data-ttu-id="52e22-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="52e22-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52e22-112">**Nome**</span><span class="sxs-lookup"><span data-stu-id="52e22-112">**Name**</span></span> <br/> |<span data-ttu-id="52e22-113">Uma cadeia de caracteres que identifica o campo.</span><span class="sxs-lookup"><span data-stu-id="52e22-113">A string that identifies the field.</span></span>  <br/> |
|<span data-ttu-id="52e22-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="52e22-114">**Value**</span></span> <br/> |<span data-ttu-id="52e22-115">Uma expressão que especifica o valor a ser atribuído ao campo.</span><span class="sxs-lookup"><span data-stu-id="52e22-115">An expression that specifies the value to assign to the field.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52e22-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="52e22-116">Remarks</span></span>

<span data-ttu-id="52e22-117">A ação **SetField** não pode ser usada fora de um bloco de dados **[CriarRegistro](createrecord-data-block-access-custom-web-app.md)** ou **[editarregistro](editrecord-data-block-access-custom-web-app.md)** .</span><span class="sxs-lookup"><span data-stu-id="52e22-117">The **SetField** action cannot be used outside of a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block.</span></span> 
  

