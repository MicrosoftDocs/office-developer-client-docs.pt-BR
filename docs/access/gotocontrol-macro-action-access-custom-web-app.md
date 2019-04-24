---
title: Ação de macro IrParaControle (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: Use a ação IrParaControle para mover o foco para o controle especificado no registro atual da exibição aberta.
ms.openlocfilehash: 2368933a6277615554a565d3bdd973f7d1f366f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302573"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a><span data-ttu-id="b41a7-103">Ação de macro IrParaControle (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="b41a7-103">GoToControl Macro Action (Access custom web app)</span></span>

<span data-ttu-id="b41a7-104">Use a ação **IrParaControle** para mover o foco para o controle especificado no registro atual da exibição aberta.</span><span class="sxs-lookup"><span data-stu-id="b41a7-104">You can use the **GoToControl** action to move the focus to the specified control in the current record of the open view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="b41a7-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="b41a7-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="b41a7-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="b41a7-107">Setting</span></span>

<span data-ttu-id="b41a7-108">A ação **IrParaControle** tem os argumentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b41a7-108">The **GoToControl** action has the following argument.</span></span> 
  
|<span data-ttu-id="b41a7-109">**Argumento da ação**</span><span class="sxs-lookup"><span data-stu-id="b41a7-109">**Action argument**</span></span>|<span data-ttu-id="b41a7-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b41a7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b41a7-111">**Nome do Controle**</span><span class="sxs-lookup"><span data-stu-id="b41a7-111">**Control Name**</span></span> <br/> |<span data-ttu-id="b41a7-112">O nome do campo ou do controle em que você deseja focar.</span><span class="sxs-lookup"><span data-stu-id="b41a7-112">The name of the field or control where you want the focus.</span></span> <span data-ttu-id="b41a7-113">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="b41a7-113">This is a required argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b41a7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b41a7-114">Remarks</span></span>

<span data-ttu-id="b41a7-115">Use esta ação quando quiser que um campo ou controle específico tenha o foco.</span><span class="sxs-lookup"><span data-stu-id="b41a7-115">You can use this action when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="b41a7-116">Você também pode usar esta ação para navegar em um formulário de acordo com certas condições.</span><span class="sxs-lookup"><span data-stu-id="b41a7-116">You can also use this action to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="b41a7-117">Por exemplo, se o usuário inserir Não em um controle Casado de um formulário de seguro de saúde, o foco automaticamente poderá ignorar o controle Nome do cônjuge/parceiro e passar para o próximo controle.</span><span class="sxs-lookup"><span data-stu-id="b41a7-117">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>
  

