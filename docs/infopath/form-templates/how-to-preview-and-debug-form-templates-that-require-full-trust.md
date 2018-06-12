---
title: Visualizar e depurar os modelos de formulário que exijam confiança total
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- depuração de modelos de formulário do [infopath 2007], infopath 2003 compatíveis, visualização de modelos de formulário compatíveis com o InfoPath 2003, modelos de formulário [InfoPath 2007], visualização 2003 compatíveis, 2003 compatíveis, depuração de depuração de modelos de formulário [InfoPath 2007] Modelos de formulário compatíveis com o InfoPath 2003
localization_priority: Normal
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: Por padrão, se você tentar depurar ou projeto de visualização de um código gerenciado que contém o código que invoca um membro de modelo de objeto que requer confiança total, tais como a propriedade LoginName que exige acesso a informações sobre o domínio de logon do usuário, Microsoft InfoPath exibirá as seguintes mensagens de erro.
ms.openlocfilehash: e9077b4ec0f8369b869e986020e4860f325fc023
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765602"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a><span data-ttu-id="8f553-104">Visualizar e depurar os modelos de formulário que exijam confiança total</span><span class="sxs-lookup"><span data-stu-id="8f553-104">Preview and Debug Form Templates that Require Full Trust</span></span>

<span data-ttu-id="8f553-105">Por padrão, se você tentar depurar ou projeto de visualização de um código gerenciado que contém o código que invoca um membro de modelo de objeto que requer confiança total, tais como a propriedade **LoginName** que exige acesso a informações sobre o domínio de logon do usuário, Microsoft InfoPath exibirá as seguintes mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="8f553-105">By default, if you attempt to debug or preview a managed-code project that contains code that invokes an object model member that requires full trust, such as the **LoginName** property which requires access to information about the user's login domain, Microsoft InfoPath will display the following error messages.</span></span> 
  
<span data-ttu-id="8f553-106">Ao pré-visualizar:</span><span class="sxs-lookup"><span data-stu-id="8f553-106">When previewing:</span></span>
  
<span data-ttu-id="8f553-107">"Uma exceção não tratada ocorreu no código do formulário."</span><span class="sxs-lookup"><span data-stu-id="8f553-107">"An unhandled exception has occurred in the form's code."</span></span> <span data-ttu-id="8f553-108">Seguido, "InfoPath não é possível concluir esta ação, devido a um erro no código do formulário."</span><span class="sxs-lookup"><span data-stu-id="8f553-108">Followed by, "InfoPath cannot complete this action, because of an error in the form's code."</span></span>
  
<span data-ttu-id="8f553-109">Quando estiver depurando:</span><span class="sxs-lookup"><span data-stu-id="8f553-109">When debugging:</span></span>
  
<span data-ttu-id="8f553-110">Foco será movido para a linha de código no editor de código que está chamando o membro que requer confiança total, e a seguinte mensagem será exibida: **"SecurityException** não foi tratada pelo código de usuário - falha na solicitação".</span><span class="sxs-lookup"><span data-stu-id="8f553-110">Focus will move to the line of code in the code editor that is calling the member that requires full trust, and the following message will be displayed: " **SecurityException** was unhandled by user code - Request failed".</span></span> 
  
<span data-ttu-id="8f553-111">Para permitir que a lógica de negócios do modelo de formulário chamar esse membro quando ele estiver sendo depurados ou visualizados, você deve definir o nível de segurança do modelo de formulário como **Confiança total** conforme descrito no procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="8f553-111">To allow the form template's business logic to call this member when it is being debugged or previewed, you must set your form template's security level to **Full Trust** as described in the following procedure.</span></span> 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a><span data-ttu-id="8f553-112">Configurando um modelo de formulário de código gerenciado que requer confiança total</span><span class="sxs-lookup"><span data-stu-id="8f553-112">Configuring a Managed Code Form Template that Requires Full Trust</span></span>

### <a name="set-your-forms-security-level-to-full-trust"></a><span data-ttu-id="8f553-113">Definir o nível de segurança do seu formulário como confiança total</span><span class="sxs-lookup"><span data-stu-id="8f553-113">Set your form's security level to Full Trust</span></span>

1. <span data-ttu-id="8f553-114">No InfoPath, abra o modelo de formulário no modo de design.</span><span class="sxs-lookup"><span data-stu-id="8f553-114">In InfoPath, open the form template in design mode.</span></span>
    
2. <span data-ttu-id="8f553-115">Clique na guia **arquivo** e clique em **Opções de formulário** , na guia **informações** .</span><span class="sxs-lookup"><span data-stu-id="8f553-115">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="8f553-116">Na lista **categoria** , clique em **Security e Trust.**</span><span class="sxs-lookup"><span data-stu-id="8f553-116">In the **Category** list, click **Security and Trust.**</span></span>
    
4. <span data-ttu-id="8f553-117">Em **Nível de segurança**, desmarque a **determinar o nível de segurança automaticamente**.</span><span class="sxs-lookup"><span data-stu-id="8f553-117">Under **Security Level**, clear **Automatically determine security level**.</span></span>
    
5. <span data-ttu-id="8f553-118">Selecione a **Confiança total**e clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="8f553-118">Select **Full Trust**, and then click **OK**.</span></span>
    
<span data-ttu-id="8f553-119">Depois que esse procedimento é executado, você pode depurar seu projeto, conforme descrito em [Visualizar e depurar modelos de formulário do InfoPath com código](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="8f553-119">After this procedure is performed, you can debug your project as described in [Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="8f553-120">Implantando com êxito um modelo de formulário de código gerenciado que requer confiança total requer etapas adicionais, como assinar digitalmente, ou instalar e registrar o modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="8f553-120">Successfully deploying a managed code form template that requires full trust requires additional steps, such as digitally signing, or installing and registering the form template.</span></span> <span data-ttu-id="8f553-121">Para obter informações sobre como implantar um modelo de formulário de código gerenciado depois que ele é depurado ver, [Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="8f553-121">For information on deploying a managed code form template after it is debugged see, [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8f553-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f553-122">See also</span></span>



[<span data-ttu-id="8f553-123">Visualizar e depurar os modelos de formulário do InfoPath com código</span><span class="sxs-lookup"><span data-stu-id="8f553-123">Preview and Debug InfoPath Form Templates with Code</span></span>](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[<span data-ttu-id="8f553-124">Implantar modelos de formulário do InfoPath com código</span><span class="sxs-lookup"><span data-stu-id="8f553-124">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)

