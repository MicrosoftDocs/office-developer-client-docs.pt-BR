---
title: Ação de macro IrParaControle (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: Use a ação IrParaControle para mover o foco para o controle especificado no registro atual da exibição aberta.
ms.openlocfilehash: ec156d1eb6c510ee38c0268a7b0f51bdde80f887
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765060"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a><span data-ttu-id="58aad-103">Ação de macro IrParaControle (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="58aad-103">GoToControl Macro Action (Access custom web app)</span></span>

<span data-ttu-id="58aad-104">Use a ação **IrParaControle** para mover o foco para o controle especificado no registro atual da exibição aberta.</span><span class="sxs-lookup"><span data-stu-id="58aad-104">You can use the **GoToControl** action to move the focus to the specified control in the current record of the open view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="58aad-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/pt-BR/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="58aad-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/pt-BR/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="58aad-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="58aad-107">Setting</span></span>

<span data-ttu-id="58aad-108">A ação **IrParaControle** tem os argumentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="58aad-108">The **OpenDiagram** action has the following argument.</span></span> 
  
|<span data-ttu-id="58aad-109">**Argumento da ação**</span><span class="sxs-lookup"><span data-stu-id="58aad-109">**Action argument**</span></span>|<span data-ttu-id="58aad-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="58aad-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="58aad-111">**Nome do Controle**</span><span class="sxs-lookup"><span data-stu-id="58aad-111">**Control Name**</span></span> <br/> |<span data-ttu-id="58aad-112">O nome do campo ou do controle em que você deseja focar.</span><span class="sxs-lookup"><span data-stu-id="58aad-112">The name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="58aad-113">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="58aad-113">This is a required argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58aad-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="58aad-114">Remarks</span></span>

<span data-ttu-id="58aad-115">Use esta ação quando quiser que um campo ou controle específico tenha o foco.</span><span class="sxs-lookup"><span data-stu-id="58aad-115">You can use the SetFocus method when you want a particular field or control to have the focus so that all user input is directed to this object.</span></span> <span data-ttu-id="58aad-116">Você também pode usar esta ação para navegar em um formulário de acordo com certas condições.</span><span class="sxs-lookup"><span data-stu-id="58aad-116">You can also use the SetFocus method to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="58aad-117">Por exemplo, se o usuário inserir Não em um controle Casado de um formulário de seguro de saúde, o foco automaticamente poderá ignorar o controle Nome do cônjuge/parceiro e passar para o próximo controle.</span><span class="sxs-lookup"><span data-stu-id="58aad-117">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>
  

