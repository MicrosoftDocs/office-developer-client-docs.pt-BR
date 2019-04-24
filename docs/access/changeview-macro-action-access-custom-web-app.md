---
title: Ação de macro ChangeView (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Você pode usar a ação ChangeView para navegar entre modos de exibição no local.
ms.openlocfilehash: 0c1e27c264a826d38ec2efbd5be9bc6237ad7437
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282310"
---
# <a name="changeview-macro-action-access-custom-web-app"></a><span data-ttu-id="a8c2c-103">Ação de macro ChangeView (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="a8c2c-103">ChangeView Macro Action (Access custom web app)</span></span>

<span data-ttu-id="a8c2c-104">Você pode usar a ação **ChangeView** para navegar entre modos de exibição no local.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-104">You can use the **ChangeView** action to navigate between views in place.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="a8c2c-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="a8c2c-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="a8c2c-107">Setting</span></span>

<span data-ttu-id="a8c2c-108">A ação **ChangeView** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-108">The **ChangeView** action has the following arguments.</span></span> 
  
|<span data-ttu-id="a8c2c-109">**Argumento da ação**</span><span class="sxs-lookup"><span data-stu-id="a8c2c-109">**Action argument**</span></span>|<span data-ttu-id="a8c2c-110">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="a8c2c-110">**Required**</span></span>|<span data-ttu-id="a8c2c-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a8c2c-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a8c2c-112">Tabela</span><span class="sxs-lookup"><span data-stu-id="a8c2c-112">Table</span></span>  <br/> |<span data-ttu-id="a8c2c-113">Sim</span><span class="sxs-lookup"><span data-stu-id="a8c2c-113">Yes</span></span>  <br/> |<span data-ttu-id="a8c2c-114">O nome da tabela que será aberta.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-114">The name of the table to open.</span></span>  <br/> |
|<span data-ttu-id="a8c2c-115">Exibir</span><span class="sxs-lookup"><span data-stu-id="a8c2c-115">View</span></span>  <br/> |<span data-ttu-id="a8c2c-116">Sim</span><span class="sxs-lookup"><span data-stu-id="a8c2c-116">Yes</span></span>  <br/> |<span data-ttu-id="a8c2c-117">O nome do modo de exibição que será aberto.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-117">The name of the view to open.</span></span>  <br/> |
|<span data-ttu-id="a8c2c-118">Em que</span><span class="sxs-lookup"><span data-stu-id="a8c2c-118">Where</span></span>  <br/> |<span data-ttu-id="a8c2c-119">Não</span><span class="sxs-lookup"><span data-stu-id="a8c2c-119">No</span></span>  <br/> |<span data-ttu-id="a8c2c-120">Se estiver especificado, substitui a condição Where da fonte de registro de objeto.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-120">If specified, replaces the Where condition of the object record source.</span></span>  <br/> |
|<span data-ttu-id="a8c2c-121">Classificado Por</span><span class="sxs-lookup"><span data-stu-id="a8c2c-121">Order By</span></span>  <br/> |<span data-ttu-id="a8c2c-122">Não</span><span class="sxs-lookup"><span data-stu-id="a8c2c-122">No</span></span>  <br/> |<span data-ttu-id="a8c2c-123">Uma expressão de cadeia de caracteres que inclui o nome do(s) campo(s) no(s) qual(is) serão classificados os registros e as palavras-chave CRESC ou DECRESC opcionais.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-123">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="a8c2c-124">Por padrão, esse argumento fica em branco.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-124">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8c2c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8c2c-125">Remarks</span></span>

<span data-ttu-id="a8c2c-126">Qualquer classificação ou filtragem aplicada pelo usuário é desmarcada quando a ação **ChangeView** é chamada.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-126">Any sorting or filtering applied by the user is cleared when the **ChangeView** action is called.</span></span> 
  
<span data-ttu-id="a8c2c-127">O argumento *OrderBy* é o nome do campo ou dos campos nos quais você deseja classificar registros.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-127">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="a8c2c-128">Quando você usa mais de um nome de campo, separe-os com uma vírgula (,).</span><span class="sxs-lookup"><span data-stu-id="a8c2c-128">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="a8c2c-129">Quando você define o argumento *OrderBy* , os registros são classificados por padrão em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-129">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

