---
title: Ação de macro ChangeView (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Você pode usar a ação ChangeView para navegar entre os exibições no local.
ms.openlocfilehash: 0c1e27c264a826d38ec2efbd5be9bc6237ad7437
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425355"
---
# <a name="changeview-macro-action-access-custom-web-app"></a><span data-ttu-id="5ac1f-103">Ação de macro ChangeView (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="5ac1f-103">ChangeView Macro Action (Access custom web app)</span></span>

<span data-ttu-id="5ac1f-104">Você pode usar a **ação ChangeView** para navegar entre os exibições no local.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-104">You can use the **ChangeView** action to navigate between views in place.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="5ac1f-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="5ac1f-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="5ac1f-107">Setting</span></span>

<span data-ttu-id="5ac1f-108">A **ação ChangeView** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-108">The **ChangeView** action has the following arguments.</span></span> 
  
|<span data-ttu-id="5ac1f-109">**Argumento da ação**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-109">**Action argument**</span></span>|<span data-ttu-id="5ac1f-110">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-110">**Required**</span></span>|<span data-ttu-id="5ac1f-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5ac1f-112">Table</span><span class="sxs-lookup"><span data-stu-id="5ac1f-112">Table</span></span>  <br/> |<span data-ttu-id="5ac1f-113">Sim</span><span class="sxs-lookup"><span data-stu-id="5ac1f-113">Yes</span></span>  <br/> |<span data-ttu-id="5ac1f-114">O nome da tabela que será aberta.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-114">The name of the table to open.</span></span>  <br/> |
|<span data-ttu-id="5ac1f-115">Exibir</span><span class="sxs-lookup"><span data-stu-id="5ac1f-115">View</span></span>  <br/> |<span data-ttu-id="5ac1f-116">Sim</span><span class="sxs-lookup"><span data-stu-id="5ac1f-116">Yes</span></span>  <br/> |<span data-ttu-id="5ac1f-117">O nome do modo de exibição que será aberto.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-117">The name of the view to open.</span></span>  <br/> |
|<span data-ttu-id="5ac1f-118">Em que</span><span class="sxs-lookup"><span data-stu-id="5ac1f-118">Where</span></span>  <br/> |<span data-ttu-id="5ac1f-119">Não</span><span class="sxs-lookup"><span data-stu-id="5ac1f-119">No</span></span>  <br/> |<span data-ttu-id="5ac1f-120">Se estiver especificado, substitui a condição Where da fonte de registro de objeto.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-120">If specified, replaces the Where condition of the object record source.</span></span>  <br/> |
|<span data-ttu-id="5ac1f-121">Classificado Por</span><span class="sxs-lookup"><span data-stu-id="5ac1f-121">Order By</span></span>  <br/> |<span data-ttu-id="5ac1f-122">Não</span><span class="sxs-lookup"><span data-stu-id="5ac1f-122">No</span></span>  <br/> |<span data-ttu-id="5ac1f-123">Uma expressão de cadeia de caracteres que inclui o nome do(s) campo(s) no(s) qual(is) serão classificados os registros e as palavras-chave CRESC ou DECRESC opcionais.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-123">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="5ac1f-124">Por padrão, esse argumento fica em branco.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-124">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ac1f-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ac1f-125">Remarks</span></span>

<span data-ttu-id="5ac1f-126">Qualquer classificação ou filtragem aplicada pelo usuário é limpa quando a **ação ChangeView** é chamada.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-126">Any sorting or filtering applied by the user is cleared when the **ChangeView** action is called.</span></span> 
  
<span data-ttu-id="5ac1f-127">O  *argumento OrderBy*  é o nome do campo ou dos campos nos quais você deseja classificar registros.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-127">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="5ac1f-128">Quando você usa mais de um nome de campo, separe-os com uma vírgula (,).</span><span class="sxs-lookup"><span data-stu-id="5ac1f-128">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="5ac1f-129">Quando você definir o  *argumento OrderBy,*  os registros serão organizados por padrão em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-129">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

