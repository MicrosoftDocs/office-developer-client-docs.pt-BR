---
title: Ação de Macro GoToControl (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: Você pode usar a ação GoToControl para mover o foco para o controle especificado no registro atual do modo de exibição aberto.
ms.openlocfilehash: ec156d1eb6c510ee38c0268a7b0f51bdde80f887
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765060"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a><span data-ttu-id="29afc-103">Ação de Macro GoToControl (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="29afc-103">GoToControl Macro Action (Access custom web app)</span></span>

<span data-ttu-id="29afc-104">Você pode usar a ação **GoToControl** para mover o foco para o controle especificado no registro atual do modo de exibição aberto.</span><span class="sxs-lookup"><span data-stu-id="29afc-104">You can use the **GoToControl** action to move the focus to the specified control in the current record of the open view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="29afc-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="29afc-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="29afc-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="29afc-107">Setting</span></span>

<span data-ttu-id="29afc-108">A ação **GoToControl** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="29afc-108">The **GoToControl** action has the following argument.</span></span> 
  
|<span data-ttu-id="29afc-109">**Argumento da ação**</span><span class="sxs-lookup"><span data-stu-id="29afc-109">**Action argument**</span></span>|<span data-ttu-id="29afc-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="29afc-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="29afc-111">**Nome do controle**</span><span class="sxs-lookup"><span data-stu-id="29afc-111">**Control Name**</span></span> <br/> |<span data-ttu-id="29afc-112">O nome do campo ou controle onde você deseja que o foco.</span><span class="sxs-lookup"><span data-stu-id="29afc-112">The name of the field or control where you want the focus.</span></span> <span data-ttu-id="29afc-113">Esse é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="29afc-113">This is a required argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29afc-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="29afc-114">Remarks</span></span>

<span data-ttu-id="29afc-115">Você pode usar essa ação quando quiser que um determinado campo ou controle tenha o foco.</span><span class="sxs-lookup"><span data-stu-id="29afc-115">You can use this action when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="29afc-116">Você também pode usar essa ação para navegar em um formulário de acordo com certas condições.</span><span class="sxs-lookup"><span data-stu-id="29afc-116">You can also use this action to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="29afc-117">Por exemplo, se o usuário digitar não em um controle Casado em um formulário de seguro saúde, o foco pode automaticamente ignorar o controle nome do cônjuge e mover para o próximo controle.</span><span class="sxs-lookup"><span data-stu-id="29afc-117">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>
  

