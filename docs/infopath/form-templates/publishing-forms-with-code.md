---
title: Publicar formulários com código
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: caafab24-6413-4731-813d-cba3ae9ea97e
description: Qualquer administrador de conjunto de sites pode publicar formulários com código diretamente do assistente de publicação do InfoPath designer para uma biblioteca de formulários no SharePoint. O código é executado em um ambiente de área restrita para que o código mal-intencionado não possa danificar o servidor. Isso é conhecido como publicação de uma solução em área restrita ou publicação na infraestrutura de área restrita do SharePoint.
ms.openlocfilehash: f8f8a48ea6810b5331198f6ddc112b3bd38ab886
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428323"
---
# <a name="publishing-forms-with-code"></a>Publicar formulários com código

Qualquer administrador de conjunto de sites pode publicar formulários com código diretamente do assistente de publicação do InfoPath designer para uma biblioteca de formulários no SharePoint. O código é executado em um ambiente de área restrita para que o código mal-intencionado não possa danificar o servidor. Isso é conhecido como publicação de uma solução em área restrita ou publicação na infraestrutura de área restrita do SharePoint.
  
O InfoPath 2010 e o SharePoint Server 2010 também oferecem suporte a soluções implantadas pelo administrador. Um designer de formulários publica formulários com código em um repositório local que é revisado e carregado posteriormente por um administrador de farm do SharePoint. O código recebe confiança total e pode incorporar funcionalidades que exigem privilégios elevados, como e/s de arquivo.
  
## <a name="comparing-sandboxed-and-administrator-approved-solutions"></a>ComParando soluções de área restrita e aprovadas pelo administrador

A tabela a seguir resume as diferenças entre a publicação de soluções de área restrita e aprovada pelo administrador. 
  
||**Soluções de área restrita**|**Soluções aprovadas pelo administrador**|
|:-----|:-----|:-----|
|**Permissões necessárias** <br/> |Pode ser publicado por qualquer administrador de conjunto de sites.  <br/> |Pode ser implantado por um administrador de farm.  <br/> |
|**Publicação** <br/> |Pode ser publicado diretamente do InfoPath.  <br/> |O pode ser implantado usando a administração central ou a ferramenta de linha de comando Stsadm.  <br/> |
|**Protection** <br/> |O código é executado em um ambiente de área restrita. Isso ajuda a proteger o servidor de código mal-intencionado.  <br/> |O código pode ser executado com confiança total e acessar qualquer recurso no servidor.  <br/> |
|**Uso recomendado** <br/> |Formulários que exigem apenas uma pequena quantidade de código.  <br/> |Formulários que contêm muitas linhas de código.  <br/> |
   
### <a name="publishing-form-templates-as-sandboxed-solutions"></a>Publicar modelos de formulário como soluções de área restrita

Publicar um formulário com código como uma solução de área restrita não é diferente de publicar qualquer outro formulário em uma biblioteca de documentos. Basta usar o assistente de publicação normalmente e o formulário será carregado no servidor e funcionará na área restrita.
  
Observe que há certas restrições para implantar seu formulário como uma solução de área restrita:
  
- Deve ser um formulário do InfoPath.
    
- O deve usar C# ou Visual Basic como linguagem de programação.
    
- Não é possível enviar para conexões de dados de email.
    
- Não é possível ter propriedades promovidas para conexões de parte para parte.
    
- Não deve ter controles de metadados ou conexões de dados gerenciados.
    
Para permitir que os administradores de conjunto de sites usem soluções de área restrita no Microsoft SharePoint Server 2010 ou em um servidor que executa o Microsoft SharePoint Foundation 2010, o administrador do farm deve iniciar o serviço de código de usuário do Windows SharePoint.
  
### <a name="to-start-the-windows-sharepoint-user-code-service"></a>Para iniciar o serviço de código de usuário do Windows SharePoint

1. Abra Administração Central.
    
2. Em **Serviços do sistema**, clique em **gerenciar serviços no servidor**.
    
3. Inicie o **serviço de código de usuário do Microsoft SharePoint Foundation**.
    
### <a name="to-publish-a-sandboxed-solution"></a>Para publicar uma solução em área restrita

1. Abra o modelo de formulário no designer do InfoPath.
    
2. Clique na guia **arquivo** e, em seguida, clique em **SharePoint Server** na guia **publicar** no backstage. 
    
3. Insira a URL do site do SharePoint para publicar e clique em **Avançar**. 
    
    > [!IMPORTANT]
    > Você deve ser um administrador de conjunto de sites neste site para publicar este modelo de formulário como uma solução de área restrita. 
  
4. Selecione **biblioteca de formulários**e clique em **Avançar**.
    
5. Selecione **criar uma nova biblioteca de formulários**e clique em **Avançar**.
    
6. Insira o nome e as descrições da sua biblioteca de formulários e clique em **Avançar**.
    
7. Clique em **publicar**.
    
Por exemplos de soluções que demonstram cenários que são apropriados para modelos de formulário publicados como soluções de área restrita, consulte [Sample sandboxEd Solutions](sample-sandboxed-solutions.md).
  
### <a name="publishing-form-templates-as-administrator-deployed-solutions"></a>Publicar modelos de formulário como soluções imPlantadas pelo administrador

É recomendável publicar o formulário como um modelo aprovado pelo administrador se o formulário tiver muitas conexões de dados, se ele exigir segurança de confiança total ou se você precisar de um modelo de todo o farm.
  
Há várias etapas que um administrador de farm deve concluir antes que uma solução implantada pelo administrador esteja disponível no SharePoint, e você como o desenvolvedor deve preparar a solução antes que o administrador seja envolvido.
  
Primeiro, se o formulário for implantado como confiança total, você deve definir o nível de segurança conforme descrito no procedimento a seguir.
  
### <a name="to-set-the-security-level-of-a-form-template-to-full-trust"></a>Para definir o nível de segurança de um modelo de formulário como confiança total

1. Abra o modelo de formulário no designer do InfoPath.
    
2. Clique na guia **arquivo** , na guia **informações** , clique em **Opções de formulário**.
    
3. Clique na categoria **segurança e confiança** e desmarque a caixa de seleção **determinar automaticamente o nível de segurança** . 
    
4. Selecione **confiança total**.
    
Em seguida, publique o formulário usando o procedimento a seguir, mas saiba que há algumas diferenças de um procedimento de publicação padrão.
  
### <a name="to-publish-an-administrator-deployed-solution"></a>Para publicar uma solução implantada pelo administrador

1. Na primeira página do assistente de **publicação**, especifique o local do site do sharepoint Server 2010 ou sharepoint Foundation 2010 e clique em **Avançar**.
    
2. O InfoPath selecionará automaticamente a caixa de seleção **modelo de formulário aprovado pelo administrador** na segunda página do assistente. Clique em **Avançar**.
    
3. A terceira página é exclusiva para cenários implantados pelo administrador. Em vez de selecionar um SharePoint Server, publique o formulário em um repositório local. O administrador do SharePoint carregará o arquivo deste local durante o processo de implantação do administrador.
    
4. Preencha as páginas restantes do **Assistente de publicação**.
    

