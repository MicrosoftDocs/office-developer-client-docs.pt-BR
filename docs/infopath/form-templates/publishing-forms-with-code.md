---
title: Publicar formulários com código
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: caafab24-6413-4731-813d-cba3ae9ea97e
description: Qualquer administrador de conjunto de sites pode publicar formulários com código diretamente do assistente de publicação do InfoPath Designer em uma biblioteca de formulários no SharePoint. O código é executado em um ambiente em áreas de segurança para que código mal-intencionado não possa prejudicar o servidor. Isso é conhecido como publicação de uma solução em áreas de segurança ou publicação na infraestrutura de áreas de segurança do SharePoint.
ms.openlocfilehash: f8f8a48ea6810b5331198f6ddc112b3bd38ab886
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428323"
---
# <a name="publishing-forms-with-code"></a><span data-ttu-id="c1f19-105">Publicar formulários com código</span><span class="sxs-lookup"><span data-stu-id="c1f19-105">Publishing Forms with Code</span></span>

<span data-ttu-id="c1f19-106">Qualquer administrador de conjunto de sites pode publicar formulários com código diretamente do assistente de publicação do InfoPath Designer em uma biblioteca de formulários no SharePoint.</span><span class="sxs-lookup"><span data-stu-id="c1f19-106">Any site collection administrator can publish forms with code directly from the InfoPath Designer publishing wizard to a form library on SharePoint.</span></span> <span data-ttu-id="c1f19-107">O código é executado em um ambiente em áreas de segurança para que código mal-intencionado não possa prejudicar o servidor.</span><span class="sxs-lookup"><span data-stu-id="c1f19-107">The code is executed in a sandboxed environment so that malicious code cannot harm the server.</span></span> <span data-ttu-id="c1f19-108">Isso é conhecido como publicação de uma solução em áreas de segurança ou publicação na infraestrutura de áreas de segurança do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="c1f19-108">This is referred to as publishing a sandboxed solution or publishing to the SharePoint sandbox infrastructure.</span></span>
  
<span data-ttu-id="c1f19-109">O InfoPath 2010 e o SharePoint Server 2010 também suportam soluções implantadas pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="c1f19-109">InfoPath 2010 and SharePoint Server 2010 also support administrator-deployed solutions.</span></span> <span data-ttu-id="c1f19-110">Um designer de formulários publica formulários com código em um armazenamento local que são revisados e carregados posteriormente por um administrador de farm do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="c1f19-110">A form designer publishes forms with code to a local store which are later reviewed and uploaded by a SharePoint farm administrator.</span></span> <span data-ttu-id="c1f19-111">O código recebe confiança total e pode incorporar funcionalidades que exigem privilégios elevados, como E/S de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c1f19-111">The code is given full trust, and can incorporate functionality requiring elevated privileges such as file IO.</span></span>
  
## <a name="comparing-sandboxed-and-administrator-approved-solutions"></a><span data-ttu-id="c1f19-112">Comparando soluções de áreas de segurança e aprovadas pelo administrador</span><span class="sxs-lookup"><span data-stu-id="c1f19-112">Comparing Sandboxed and Administrator-approved Solutions</span></span>

<span data-ttu-id="c1f19-113">A tabela a seguir resume as diferenças entre a publicação de soluções de área de segurança e aprovadas pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="c1f19-113">The following table summarizes the differences between publishing sandboxed and administrator-approved solutions.</span></span> 
  
||<span data-ttu-id="c1f19-114">**Soluções de área restrita**</span><span class="sxs-lookup"><span data-stu-id="c1f19-114">**Sandboxed Solutions**</span></span>|<span data-ttu-id="c1f19-115">**Soluções aprovadas pelo administrador**</span><span class="sxs-lookup"><span data-stu-id="c1f19-115">**Administrator-approved Solutions**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c1f19-116">**Permissões necessárias**</span><span class="sxs-lookup"><span data-stu-id="c1f19-116">**Permissions Required**</span></span> <br/> |<span data-ttu-id="c1f19-117">Pode ser publicado por qualquer administrador de conjunto de sites.</span><span class="sxs-lookup"><span data-stu-id="c1f19-117">Can be published by any site collection administrator.</span></span>  <br/> |<span data-ttu-id="c1f19-118">Pode ser implantado por um administrador de farm.</span><span class="sxs-lookup"><span data-stu-id="c1f19-118">Can be deployed by a farm administrator.</span></span>  <br/> |
|<span data-ttu-id="c1f19-119">**Publicação**</span><span class="sxs-lookup"><span data-stu-id="c1f19-119">**Publishing**</span></span> <br/> |<span data-ttu-id="c1f19-120">Pode ser publicado diretamente do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="c1f19-120">Can be published directly from InfoPath.</span></span>  <br/> |<span data-ttu-id="c1f19-121">Pode ser implantada usando a Administração Central ou a ferramenta de linha de comando stsadm.</span><span class="sxs-lookup"><span data-stu-id="c1f19-121">Can be deployed using Central Administration or the stsadm command-line tool.</span></span>  <br/> |
|<span data-ttu-id="c1f19-122">**Protection**</span><span class="sxs-lookup"><span data-stu-id="c1f19-122">**Protection**</span></span> <br/> |<span data-ttu-id="c1f19-123">O código é executado em um ambiente em áreas de segurança.</span><span class="sxs-lookup"><span data-stu-id="c1f19-123">Code is run in a sandboxed environment.</span></span> <span data-ttu-id="c1f19-124">Isso ajuda a proteger o servidor contra código mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="c1f19-124">This helps protect the server from malicious code.</span></span>  <br/> |<span data-ttu-id="c1f19-125">O código pode ser executado com confiança total e acessar qualquer recurso no servidor.</span><span class="sxs-lookup"><span data-stu-id="c1f19-125">Code can run with full trust and access any resource on the server.</span></span>  <br/> |
|<span data-ttu-id="c1f19-126">**Uso Recomendado**</span><span class="sxs-lookup"><span data-stu-id="c1f19-126">**Recommended Use**</span></span> <br/> |<span data-ttu-id="c1f19-127">Formulários que exigem apenas uma pequena quantidade de código.</span><span class="sxs-lookup"><span data-stu-id="c1f19-127">Forms that only require a small amount of code.</span></span>  <br/> |<span data-ttu-id="c1f19-128">Formulários que contêm muitas linhas de código.</span><span class="sxs-lookup"><span data-stu-id="c1f19-128">Forms that contain many lines of code.</span></span>  <br/> |
   
### <a name="publishing-form-templates-as-sandboxed-solutions"></a><span data-ttu-id="c1f19-129">Publicar modelos de formulário como soluções em áreas de segurança</span><span class="sxs-lookup"><span data-stu-id="c1f19-129">Publishing Form Templates as Sandboxed Solutions</span></span>

<span data-ttu-id="c1f19-130">Publicar um formulário com código como uma solução em áreas de segurança não é diferente de publicar qualquer outro formulário em uma biblioteca de documentos.</span><span class="sxs-lookup"><span data-stu-id="c1f19-130">Publishing a form with code as a sandboxed solution is no different from publishing any other form to a document library.</span></span> <span data-ttu-id="c1f19-131">Basta usar o assistente de publicação como de costume, e seu formulário será carregado no servidor e funcionará na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c1f19-131">Just use the publishing wizard as usual and your form will be uploaded to the server and will operate in the sandbox.</span></span>
  
<span data-ttu-id="c1f19-132">Observe que há certas restrições para implantar seu formulário como uma solução em áreas de segurança:</span><span class="sxs-lookup"><span data-stu-id="c1f19-132">Note that there are certain restrictions to deploying your form as a sandboxed solution:</span></span>
  
- <span data-ttu-id="c1f19-133">Deve ser um formulário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="c1f19-133">Must be an InfoPath form.</span></span>
    
- <span data-ttu-id="c1f19-134">Deve usar C# ou Visual Basic como linguagem de programação.</span><span class="sxs-lookup"><span data-stu-id="c1f19-134">Must use C# or Visual Basic as the programming language.</span></span>
    
- <span data-ttu-id="c1f19-135">Não é possível enviar conexões de dados de email.</span><span class="sxs-lookup"><span data-stu-id="c1f19-135">Cannot submit to email data connections.</span></span>
    
- <span data-ttu-id="c1f19-136">Não é possível ter propriedades promovidas para conexões de parte a parte.</span><span class="sxs-lookup"><span data-stu-id="c1f19-136">Cannot have properties promoted for part-to-part connections.</span></span>
    
- <span data-ttu-id="c1f19-137">Não deve ter controles de metadados gerenciados ou conexões de dados.</span><span class="sxs-lookup"><span data-stu-id="c1f19-137">Must not have any managed meta-data controls or data connections.</span></span>
    
<span data-ttu-id="c1f19-138">Para permitir que os administradores de conjunto de sites usem soluções em modo seguro no Microsoft SharePoint Server 2010 ou em um servidor que executa o Microsoft SharePoint Foundation 2010, o administrador do farm deve iniciar o serviço de Código de Usuário do Windows SharePoint.</span><span class="sxs-lookup"><span data-stu-id="c1f19-138">To enable site collection administrators to use sandboxed solutions on Microsoft SharePoint Server 2010 or a server that runs Microsoft SharePoint Foundation 2010, the farm administrator must start the Windows SharePoint User Code service.</span></span>
  
### <a name="to-start-the-windows-sharepoint-user-code-service"></a><span data-ttu-id="c1f19-139">Para iniciar o serviço Código de Usuário do Windows SharePoint</span><span class="sxs-lookup"><span data-stu-id="c1f19-139">To start the Windows SharePoint User Code service</span></span>

1. <span data-ttu-id="c1f19-140">Abra Administração Central.</span><span class="sxs-lookup"><span data-stu-id="c1f19-140">Open Central Administration.</span></span>
    
2. <span data-ttu-id="c1f19-141">Em **Serviços do Sistema,** clique **em Gerenciar serviços no servidor.**</span><span class="sxs-lookup"><span data-stu-id="c1f19-141">Under **System Services**, click **Manage services on server**.</span></span>
    
3. <span data-ttu-id="c1f19-142">Inicie o Serviço de Código de Usuário do **Microsoft SharePoint Foundation.**</span><span class="sxs-lookup"><span data-stu-id="c1f19-142">Start the **Microsoft SharePoint Foundation User Code Service**.</span></span>
    
### <a name="to-publish-a-sandboxed-solution"></a><span data-ttu-id="c1f19-143">Para publicar uma solução em áreas de segurança</span><span class="sxs-lookup"><span data-stu-id="c1f19-143">To publish a sandboxed solution</span></span>

1. <span data-ttu-id="c1f19-144">Abra o modelo de formulário no designer do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="c1f19-144">Open the form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="c1f19-145">Clique na **guia Arquivo** e, em seguida, clique **em SharePoint Server** na guia **Publicar** no Backstage.</span><span class="sxs-lookup"><span data-stu-id="c1f19-145">Click the **File** tab, and then click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
    
3. <span data-ttu-id="c1f19-146">Insira a URL do site do SharePoint para publicar e clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="c1f19-146">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="c1f19-147">Você deve ser um administrador de conjunto de sites neste site para publicar esse modelo de formulário como uma solução em áreas de segurança.</span><span class="sxs-lookup"><span data-stu-id="c1f19-147">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
  
4. <span data-ttu-id="c1f19-148">Selecione **a Biblioteca de** Formulário e clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="c1f19-148">Select **Form Library**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="c1f19-149">Selecione **Criar uma nova biblioteca de formulário** e clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="c1f19-149">Select **Create a new form library**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="c1f19-150">Insira o nome e as descrições da biblioteca de formulário e clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="c1f19-150">Enter the name and descriptions for your form library, and then click **Next**.</span></span>
    
7. <span data-ttu-id="c1f19-151">Clique em **Publicar**.</span><span class="sxs-lookup"><span data-stu-id="c1f19-151">Click **Publish**.</span></span>
    
<span data-ttu-id="c1f19-152">For example solutions that demonstrate scenarios that are appropriate for form templates published as sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="c1f19-152">For example solutions that demonstrate scenarios that are appropriate for form templates published as sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>
  
### <a name="publishing-form-templates-as-administrator-deployed-solutions"></a><span data-ttu-id="c1f19-153">Publicação de modelos de formulário como Administrator-Deployed soluções</span><span class="sxs-lookup"><span data-stu-id="c1f19-153">Publishing Form Templates as Administrator-Deployed Solutions</span></span>

<span data-ttu-id="c1f19-154">É recomendável publicar seu formulário como um modelo aprovado pelo administrador se o formulário tiver muitas conexões de dados, se exigir segurança de confiança total ou se você precisar de um modelo de todo o farm.</span><span class="sxs-lookup"><span data-stu-id="c1f19-154">Publishing your form as an administrator-approved template is recommended if your form has many data connections, if it requires full-trust security, or if you require a farm-wide template.</span></span>
  
<span data-ttu-id="c1f19-155">Há várias etapas que um administrador de farm deve concluir antes de uma solução implantada pelo administrador estar disponível no SharePoint, e você, como desenvolvedor, deve preparar a solução antes que o administrador seja envolvido.</span><span class="sxs-lookup"><span data-stu-id="c1f19-155">There are several steps that a farm administrator must complete before an administrator-deployed solution is available on SharePoint, and you as the developer must prepare the solution before the administrator is engaged.</span></span>
  
<span data-ttu-id="c1f19-156">Primeiro, se o formulário for implantado como confiança total, você deverá definir o nível de segurança conforme descrito no procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="c1f19-156">First, if your form is going to be deployed as full trust, you must set the security level as described in the following procedure.</span></span>
  
### <a name="to-set-the-security-level-of-a-form-template-to-full-trust"></a><span data-ttu-id="c1f19-157">Para definir o nível de segurança de um modelo de formulário como confiança total</span><span class="sxs-lookup"><span data-stu-id="c1f19-157">To set the security level of a form template to full trust</span></span>

1. <span data-ttu-id="c1f19-158">Abra o modelo de formulário no designer do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="c1f19-158">Open the form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="c1f19-159">Clique na **guia Arquivo,** na guia **Informações,** clique em **Opções de Formulário.**</span><span class="sxs-lookup"><span data-stu-id="c1f19-159">Click the **File** tab, on the **Info** tab click **Form Options**.</span></span>
    
3. <span data-ttu-id="c1f19-160">Clique na **categoria Segurança e Confiança** e des limpe a caixa de seleção Determinar automaticamente o nível **de** segurança.</span><span class="sxs-lookup"><span data-stu-id="c1f19-160">Click the **Security and Trust** category, and then clear the **Automatically determine security level** check box.</span></span> 
    
4. <span data-ttu-id="c1f19-161">Selecione **Confiança Total**.</span><span class="sxs-lookup"><span data-stu-id="c1f19-161">Select **Full Trust**.</span></span>
    
<span data-ttu-id="c1f19-162">Em seguida, publique o formulário usando o procedimento a seguir, mas esteja ciente de que há algumas diferenças em relação a um procedimento de publicação padrão.</span><span class="sxs-lookup"><span data-stu-id="c1f19-162">Then, publish the form by using the following procedure, but be aware that there are some differences from a standard publishing procedure.</span></span>
  
### <a name="to-publish-an-administrator-deployed-solution"></a><span data-ttu-id="c1f19-163">Para publicar uma solução implantada pelo administrador</span><span class="sxs-lookup"><span data-stu-id="c1f19-163">To publish an administrator-deployed solution</span></span>

1. <span data-ttu-id="c1f19-164">Na primeira página do Assistente de **Publicação,** especifique o local do site do SharePoint Server 2010 ou do SharePoint Foundation 2010 e clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="c1f19-164">In the first page of the **Publishing Wizard**, specify the location of the SharePoint Server 2010 or SharePoint Foundation 2010 site, and then click **Next**.</span></span>
    
2. <span data-ttu-id="c1f19-165">O InfoPath marcará automaticamente **a caixa de seleção de** modelo de formulário aprovado pelo administrador na segunda página do assistente.</span><span class="sxs-lookup"><span data-stu-id="c1f19-165">InfoPath will automatically select the **Administrator-approved form template** check box on the second page of the wizard.</span></span> <span data-ttu-id="c1f19-166">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="c1f19-166">Click **Next**.</span></span>
    
3. <span data-ttu-id="c1f19-167">A terceira página é exclusiva para cenários implantados pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="c1f19-167">The third page is unique to administrator-deployed scenarios.</span></span> <span data-ttu-id="c1f19-168">Em vez de selecionar um SharePoint Server, publique o formulário em um armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="c1f19-168">Instead of selecting a SharePoint Server, publish the form to a local store.</span></span> <span data-ttu-id="c1f19-169">O administrador do SharePoint carregará o arquivo desse local durante o processo de implantação do administrador.</span><span class="sxs-lookup"><span data-stu-id="c1f19-169">The SharePoint administrator will upload the file from this location during the administrator deployment process.</span></span>
    
4. <span data-ttu-id="c1f19-170">Conclua as páginas restantes do **Assistente de Publicação.**</span><span class="sxs-lookup"><span data-stu-id="c1f19-170">Complete the remaining pages of the **Publishing Wizard**.</span></span>
    

