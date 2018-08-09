---
title: Publicar formulários com código
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: caafab24-6413-4731-813d-cba3ae9ea97e
description: Qualquer administrador de conjunto de sites pode publicar formulários com código diretamente a partir do Assistente de publicação do InfoPath Designer para uma biblioteca de formulários no SharePoint. O código é executado em um ambiente de área restrita para que o código mal-intencionado não pode prejudicar o servidor. Isso é conhecido como uma solução alternativa de publicação ou publicar a infraestrutura de área restrita do SharePoint.
ms.openlocfilehash: c25243a966bc1dc1a559ccf2ba58fabfadbd94a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765713"
---
# <a name="publishing-forms-with-code"></a><span data-ttu-id="69472-105">Publicar formulários com código</span><span class="sxs-lookup"><span data-stu-id="69472-105">Publishing Forms with Code</span></span>

<span data-ttu-id="69472-106">Qualquer administrador de conjunto de sites pode publicar formulários com código diretamente a partir do Assistente de publicação do InfoPath Designer para uma biblioteca de formulários no SharePoint.</span><span class="sxs-lookup"><span data-stu-id="69472-106">Any site collection administrator can publish forms with code directly from the InfoPath Designer publishing wizard to a form library on SharePoint.</span></span> <span data-ttu-id="69472-107">O código é executado em um ambiente de área restrita para que o código mal-intencionado não pode prejudicar o servidor.</span><span class="sxs-lookup"><span data-stu-id="69472-107">The code is executed in a sandboxed environment so that malicious code cannot harm the server.</span></span> <span data-ttu-id="69472-108">Isso é conhecido como uma solução alternativa de publicação ou publicar a infraestrutura de área restrita do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="69472-108">This is referred to as publishing a sandboxed solution or publishing to the SharePoint sandbox infrastructure.</span></span>
  
<span data-ttu-id="69472-109">InfoPath 2010 e o SharePoint Server 2010 também suportam soluções implantados pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="69472-109">InfoPath 2010 and SharePoint Server 2010 also support administrator-deployed solutions.</span></span> <span data-ttu-id="69472-110">Designer de formulários publica formulários com código em um repositório local que posteriormente analisado e carregados por um administrador de farm do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="69472-110">A form designer publishes forms with code to a local store which are later reviewed and uploaded by a SharePoint farm administrator.</span></span> <span data-ttu-id="69472-111">O código recebe confiança total e pode incorporar funcionalidade que exija privilégios elevados como e/s do arquivo.</span><span class="sxs-lookup"><span data-stu-id="69472-111">The code is given full trust, and can incorporate functionality requiring elevated privileges such as file IO.</span></span>
  
## <a name="comparing-sandboxed-and-administrator-approved-solutions"></a><span data-ttu-id="69472-112">Comparar as soluções de área restrita e aprovados pelo administrador</span><span class="sxs-lookup"><span data-stu-id="69472-112">Comparing Sandboxed and Administrator-approved Solutions</span></span>

<span data-ttu-id="69472-113">A tabela a seguir resume as diferenças entre a publicação de soluções em área restrita e aprovados pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="69472-113">The following table summarizes the differences between publishing sandboxed and administrator-approved solutions.</span></span> 
  
||<span data-ttu-id="69472-114">**Soluções em área restrita**</span><span class="sxs-lookup"><span data-stu-id="69472-114">**Sandboxed Solutions**</span></span>|<span data-ttu-id="69472-115">**Soluções aprovados pelo administrador**</span><span class="sxs-lookup"><span data-stu-id="69472-115">**Administrator-approved Solutions**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="69472-116">**Permissões necessárias**</span><span class="sxs-lookup"><span data-stu-id="69472-116">**Permissions Required**</span></span> <br/> |<span data-ttu-id="69472-117">Podem ser publicadas por qualquer administrador de conjunto de sites.</span><span class="sxs-lookup"><span data-stu-id="69472-117">Can be published by any site collection administrator.</span></span>  <br/> |<span data-ttu-id="69472-118">Podem ser implantados por um administrador de farm.</span><span class="sxs-lookup"><span data-stu-id="69472-118">Can be deployed by a farm administrator.</span></span>  <br/> |
|<span data-ttu-id="69472-119">**Publicação**</span><span class="sxs-lookup"><span data-stu-id="69472-119">**Publishing**</span></span> <br/> |<span data-ttu-id="69472-120">Podem ser publicadas diretamente do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="69472-120">Can be published directly from InfoPath.</span></span>  <br/> |<span data-ttu-id="69472-121">Pode ser implantado usando a Administração Central ou a ferramenta de linha de comando stsadm.</span><span class="sxs-lookup"><span data-stu-id="69472-121">Can be deployed using Central Administration or the stsadm command-line tool.</span></span>  <br/> |
|<span data-ttu-id="69472-122">**Protection**</span><span class="sxs-lookup"><span data-stu-id="69472-122">**Protection**</span></span> <br/> |<span data-ttu-id="69472-123">Código é executado em um ambiente de área restrita.</span><span class="sxs-lookup"><span data-stu-id="69472-123">Code is run in a sandboxed environment.</span></span> <span data-ttu-id="69472-124">Isso ajuda a proteger o servidor de código mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="69472-124">This helps protect the server from malicious code.</span></span>  <br/> |<span data-ttu-id="69472-125">Código pode ser executado com confiança total e acessar qualquer recurso no servidor.</span><span class="sxs-lookup"><span data-stu-id="69472-125">Code can run with full trust and access any resource on the server.</span></span>  <br/> |
|<span data-ttu-id="69472-126">**Uso recomendado**</span><span class="sxs-lookup"><span data-stu-id="69472-126">**Recommended Use**</span></span> <br/> |<span data-ttu-id="69472-127">Formulários que requerem apenas uma pequena quantidade de código.</span><span class="sxs-lookup"><span data-stu-id="69472-127">Forms that only require a small amount of code.</span></span>  <br/> |<span data-ttu-id="69472-128">Formulários que contêm várias linhas de código.</span><span class="sxs-lookup"><span data-stu-id="69472-128">Forms that contain many lines of code.</span></span>  <br/> |
   
### <a name="publishing-form-templates-as-sandboxed-solutions"></a><span data-ttu-id="69472-129">Publicação de modelos de formulário como soluções em área restrita</span><span class="sxs-lookup"><span data-stu-id="69472-129">Publishing Form Templates as Sandboxed Solutions</span></span>

<span data-ttu-id="69472-130">Publicação de um formulário com código como uma solução alternativa não é diferente de qualquer outra forma de publicação para uma biblioteca de documentos.</span><span class="sxs-lookup"><span data-stu-id="69472-130">Publishing a form with code as a sandboxed solution is no different from publishing any other form to a document library.</span></span> <span data-ttu-id="69472-131">Basta usar o Assistente de publicação como de costume e seu formulário será carregado no servidor e vai operar da área restrita.</span><span class="sxs-lookup"><span data-stu-id="69472-131">Just use the publishing wizard as usual and your form will be uploaded to the server and will operate in the sandbox.</span></span>
  
<span data-ttu-id="69472-132">Observe que não há determinadas restrições à implantação de seu formulário como uma solução em área restrita:</span><span class="sxs-lookup"><span data-stu-id="69472-132">Note that there are certain restrictions to deploying your form as a sandboxed solution:</span></span>
  
- <span data-ttu-id="69472-133">Deve ser um formulário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="69472-133">Must be an InfoPath form.</span></span>
    
- <span data-ttu-id="69472-134">Deve usar c# ou Visual Basic como a linguagem de programação.</span><span class="sxs-lookup"><span data-stu-id="69472-134">Must use C# or Visual Basic as the programming language.</span></span>
    
- <span data-ttu-id="69472-135">Não é possível enviar para conexões de dados de email.</span><span class="sxs-lookup"><span data-stu-id="69472-135">Cannot submit to email data connections.</span></span>
    
- <span data-ttu-id="69472-136">Não podem ter propriedades promovido para conexões Web Parts.</span><span class="sxs-lookup"><span data-stu-id="69472-136">Cannot have properties promoted for part-to-part connections.</span></span>
    
- <span data-ttu-id="69472-137">Não deve ter quaisquer conexões de dados ou controles de metadados gerenciados.</span><span class="sxs-lookup"><span data-stu-id="69472-137">Must not have any managed meta-data controls or data connections.</span></span>
    
<span data-ttu-id="69472-138">Para permitir que administradores do conjunto de sites usar soluções em área restrita em Microsoft SharePoint Server 2010 ou um servidor que executa o Microsoft SharePoint Foundation 2010, o administrador do farm deve iniciar o serviço de código de usuário do Windows SharePoint.</span><span class="sxs-lookup"><span data-stu-id="69472-138">To enable site collection administrators to use sandboxed solutions on Microsoft SharePoint Server 2010 or a server that runs Microsoft SharePoint Foundation 2010, the farm administrator must start the Windows SharePoint User Code service.</span></span>
  
### <a name="to-start-the-windows-sharepoint-user-code-service"></a><span data-ttu-id="69472-139">Para iniciar o serviço de código de usuário do Windows SharePoint</span><span class="sxs-lookup"><span data-stu-id="69472-139">To start the Windows SharePoint User Code service</span></span>

1. <span data-ttu-id="69472-140">Abra a Administração Central.</span><span class="sxs-lookup"><span data-stu-id="69472-140">Open Central Administration.</span></span>
    
2. <span data-ttu-id="69472-141">Em **Serviços do sistema**, clique em **Gerenciar serviços no servidor**.</span><span class="sxs-lookup"><span data-stu-id="69472-141">Under **System Services**, click **Manage services on server**.</span></span>
    
3. <span data-ttu-id="69472-142">Inicie o **serviço de código de usuário do Microsoft SharePoint Foundation**.</span><span class="sxs-lookup"><span data-stu-id="69472-142">Start the **Microsoft SharePoint Foundation User Code Service**.</span></span>
    
### <a name="to-publish-a-sandboxed-solution"></a><span data-ttu-id="69472-143">Para publicar uma solução em área restrita</span><span class="sxs-lookup"><span data-stu-id="69472-143">To publish a sandboxed solution</span></span>

1. <span data-ttu-id="69472-144">Abra o modelo de formulário no designer do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="69472-144">Open the form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="69472-145">Clique na guia **arquivo** e, em seguida, clique em **SharePoint Server** , na guia **Publicar** no Backstage.</span><span class="sxs-lookup"><span data-stu-id="69472-145">Click the **File** tab, and then click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
    
3. <span data-ttu-id="69472-146">Insira a URL do site do SharePoint para publicar e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="69472-146">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="69472-147">Você deve ser um administrador de conjunto de sites neste site para publicar esse modelo de formulário como uma solução em área restrita.</span><span class="sxs-lookup"><span data-stu-id="69472-147">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
  
4. <span data-ttu-id="69472-148">Selecione a **Biblioteca de formulários**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="69472-148">Select **Form Library**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="69472-149">Selecione **criar uma nova biblioteca de formulários**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="69472-149">Select **Create a new form library**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="69472-150">Insira o nome e as descrições para sua biblioteca de formulários e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="69472-150">Enter the name and descriptions for your form library, and then click **Next**.</span></span>
    
7. <span data-ttu-id="69472-151">Clique em **Publicar**.</span><span class="sxs-lookup"><span data-stu-id="69472-151">Click **Publish**.</span></span>
    
<span data-ttu-id="69472-152">Por exemplo, soluções que demonstram cenários que são adequados para modelos de formulário publicados como soluções em área restrita, consulte [Exemplos de soluções em área restrita](sample-sandboxed-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="69472-152">For example solutions that demonstrate scenarios that are appropriate for form templates published as sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>
  
### <a name="publishing-form-templates-as-administrator-deployed-solutions"></a><span data-ttu-id="69472-153">Publicação de modelos de formulário como soluções implantados pelo administrador</span><span class="sxs-lookup"><span data-stu-id="69472-153">Publishing Form Templates as Administrator-Deployed Solutions</span></span>

<span data-ttu-id="69472-154">Publicar o formulário como um modelo aprovado pelo administrador recomenda-se o formulário tiver várias conexões de dados, se ele requer segurança de confiança total, ou se você precisar de um modelo de todo o farm.</span><span class="sxs-lookup"><span data-stu-id="69472-154">Publishing your form as an administrator-approved template is recommended if your form has many data connections, if it requires full-trust security, or if you require a farm-wide template.</span></span>
  
<span data-ttu-id="69472-155">Há várias etapas que deve ser concluídas por um administrador do farm antes de uma solução implantados pelo administrador ficará disponível no SharePoint e você, como o desenvolvedor deve preparar a solução antes do administrador está envolvido.</span><span class="sxs-lookup"><span data-stu-id="69472-155">There are several steps that a farm administrator must complete before an administrator-deployed solution is available on SharePoint, and you as the developer must prepare the solution before the administrator is engaged.</span></span>
  
<span data-ttu-id="69472-156">Primeiro, se o seu formulário será para ser implantado como confiança total, você deve definir o nível de segurança, conforme descrito no procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="69472-156">First, if your form is going to be deployed as full trust, you must set the security level as described in the following procedure.</span></span>
  
### <a name="to-set-the-security-level-of-a-form-template-to-full-trust"></a><span data-ttu-id="69472-157">Para definir o nível de segurança de um modelo de formulário como confiança total</span><span class="sxs-lookup"><span data-stu-id="69472-157">To set the security level of a form template to full trust</span></span>

1. <span data-ttu-id="69472-158">Abra o modelo de formulário no designer do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="69472-158">Open the form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="69472-159">Clique na guia **arquivo** , na guia **informações** , clique em **Opções de formulário**.</span><span class="sxs-lookup"><span data-stu-id="69472-159">Click the **File** tab, on the **Info** tab click **Form Options**.</span></span>
    
3. <span data-ttu-id="69472-160">Clique na categoria de **segurança e confiança** e, em seguida, desmarque a caixa de seleção **determinar automaticamente o nível de segurança** .</span><span class="sxs-lookup"><span data-stu-id="69472-160">Click the **Security and Trust** category, and then clear the **Automatically determine security level** check box.</span></span> 
    
4. <span data-ttu-id="69472-161">Selecione a **confiança total**.</span><span class="sxs-lookup"><span data-stu-id="69472-161">Select **Full Trust**.</span></span>
    
<span data-ttu-id="69472-162">Em seguida, publicá-lo usando o procedimento a seguir, mas, lembre-se de que não existem algumas diferenças de um procedimento de publicação padrão.</span><span class="sxs-lookup"><span data-stu-id="69472-162">Then, publish the form by using the following procedure, but be aware that there are some differences from a standard publishing procedure.</span></span>
  
### <a name="to-publish-an-administrator-deployed-solution"></a><span data-ttu-id="69472-163">Para publicar uma solução implantados pelo administrador</span><span class="sxs-lookup"><span data-stu-id="69472-163">To publish an administrator-deployed solution</span></span>

1. <span data-ttu-id="69472-164">Na primeira página do **Assistente de publicação**, especifique o local do site do SharePoint Server 2010 ou o SharePoint Foundation 2010 e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="69472-164">In the first page of the **Publishing Wizard**, specify the location of the SharePoint Server 2010 or SharePoint Foundation 2010 site, and then click **Next**.</span></span>
    
2. <span data-ttu-id="69472-165">InfoPath selecionará automaticamente a caixa de seleção de **modelo de formulário aprovados pelo administrador** na segunda página do assistente.</span><span class="sxs-lookup"><span data-stu-id="69472-165">InfoPath will automatically select the **Administrator-approved form template** check box on the second page of the wizard.</span></span> <span data-ttu-id="69472-166">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="69472-166">Click **Next**.</span></span>
    
3. <span data-ttu-id="69472-167">A terceira página é exclusiva cenários implantados pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="69472-167">The third page is unique to administrator-deployed scenarios.</span></span> <span data-ttu-id="69472-168">Em vez de selecionar um servidor do SharePoint, publique o formulário em um repositório local.</span><span class="sxs-lookup"><span data-stu-id="69472-168">Instead of selecting a SharePoint Server, publish the form to a local store.</span></span> <span data-ttu-id="69472-169">O administrador do SharePoint carregará o arquivo a partir deste local durante o processo de implantação do administrador.</span><span class="sxs-lookup"><span data-stu-id="69472-169">The SharePoint administrator will upload the file from this location during the administrator deployment process.</span></span>
    
4. <span data-ttu-id="69472-170">Conclua as páginas restantes do **Assistente de publicação**.</span><span class="sxs-lookup"><span data-stu-id="69472-170">Complete the remaining pages of the **Publishing Wizard**.</span></span>
    

