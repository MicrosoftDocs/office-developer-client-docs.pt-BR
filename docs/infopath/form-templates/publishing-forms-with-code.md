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
# <a name="publishing-forms-with-code"></a>Publicar formulários com código

Qualquer administrador de conjunto de sites pode publicar formulários com código diretamente do assistente de publicação do InfoPath Designer em uma biblioteca de formulários no SharePoint. O código é executado em um ambiente em áreas de segurança para que código mal-intencionado não possa prejudicar o servidor. Isso é conhecido como publicação de uma solução em áreas de segurança ou publicação na infraestrutura de áreas de segurança do SharePoint.
  
O InfoPath 2010 e o SharePoint Server 2010 também suportam soluções implantadas pelo administrador. Um designer de formulários publica formulários com código em um armazenamento local que são revisados e carregados posteriormente por um administrador de farm do SharePoint. O código recebe confiança total e pode incorporar funcionalidades que exigem privilégios elevados, como E/S de arquivo.
  
## <a name="comparing-sandboxed-and-administrator-approved-solutions"></a>Comparando soluções de áreas de segurança e aprovadas pelo administrador

A tabela a seguir resume as diferenças entre a publicação de soluções de área de segurança e aprovadas pelo administrador. 
  
||**Soluções de área restrita**|**Soluções aprovadas pelo administrador**|
|:-----|:-----|:-----|
|**Permissões necessárias** <br/> |Pode ser publicado por qualquer administrador de conjunto de sites.  <br/> |Pode ser implantado por um administrador de farm.  <br/> |
|**Publicação** <br/> |Pode ser publicado diretamente do InfoPath.  <br/> |Pode ser implantada usando a Administração Central ou a ferramenta de linha de comando stsadm.  <br/> |
|**Protection** <br/> |O código é executado em um ambiente em áreas de segurança. Isso ajuda a proteger o servidor contra código mal-intencionado.  <br/> |O código pode ser executado com confiança total e acessar qualquer recurso no servidor.  <br/> |
|**Uso Recomendado** <br/> |Formulários que exigem apenas uma pequena quantidade de código.  <br/> |Formulários que contêm muitas linhas de código.  <br/> |
   
### <a name="publishing-form-templates-as-sandboxed-solutions"></a>Publicar modelos de formulário como soluções em áreas de segurança

Publicar um formulário com código como uma solução em áreas de segurança não é diferente de publicar qualquer outro formulário em uma biblioteca de documentos. Basta usar o assistente de publicação como de costume, e seu formulário será carregado no servidor e funcionará na área de trabalho.
  
Observe que há certas restrições para implantar seu formulário como uma solução em áreas de segurança:
  
- Deve ser um formulário do InfoPath.
    
- Deve usar C# ou Visual Basic como linguagem de programação.
    
- Não é possível enviar conexões de dados de email.
    
- Não é possível ter propriedades promovidas para conexões de parte a parte.
    
- Não deve ter controles de metadados gerenciados ou conexões de dados.
    
Para permitir que os administradores de conjunto de sites usem soluções em modo seguro no Microsoft SharePoint Server 2010 ou em um servidor que executa o Microsoft SharePoint Foundation 2010, o administrador do farm deve iniciar o serviço de Código de Usuário do Windows SharePoint.
  
### <a name="to-start-the-windows-sharepoint-user-code-service"></a>Para iniciar o serviço Código de Usuário do Windows SharePoint

1. Abra Administração Central.
    
2. Em **Serviços do Sistema,** clique **em Gerenciar serviços no servidor.**
    
3. Inicie o Serviço de Código de Usuário do **Microsoft SharePoint Foundation.**
    
### <a name="to-publish-a-sandboxed-solution"></a>Para publicar uma solução em áreas de segurança

1. Abra o modelo de formulário no designer do InfoPath.
    
2. Clique na **guia Arquivo** e, em seguida, clique **em SharePoint Server** na guia **Publicar** no Backstage. 
    
3. Insira a URL do site do SharePoint para publicar e clique em **Próximo.** 
    
    > [!IMPORTANT]
    > Você deve ser um administrador de conjunto de sites neste site para publicar esse modelo de formulário como uma solução em áreas de segurança. 
  
4. Selecione **a Biblioteca de** Formulário e clique em **Próximo.**
    
5. Selecione **Criar uma nova biblioteca de formulário** e clique em **Próximo.**
    
6. Insira o nome e as descrições da biblioteca de formulário e clique em **Próximo.**
    
7. Clique em **Publicar**.
    
For example solutions that demonstrate scenarios that are appropriate for form templates published as sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).
  
### <a name="publishing-form-templates-as-administrator-deployed-solutions"></a>Publicação de modelos de formulário como Administrator-Deployed soluções

É recomendável publicar seu formulário como um modelo aprovado pelo administrador se o formulário tiver muitas conexões de dados, se exigir segurança de confiança total ou se você precisar de um modelo de todo o farm.
  
Há várias etapas que um administrador de farm deve concluir antes de uma solução implantada pelo administrador estar disponível no SharePoint, e você, como desenvolvedor, deve preparar a solução antes que o administrador seja envolvido.
  
Primeiro, se o formulário for implantado como confiança total, você deverá definir o nível de segurança conforme descrito no procedimento a seguir.
  
### <a name="to-set-the-security-level-of-a-form-template-to-full-trust"></a>Para definir o nível de segurança de um modelo de formulário como confiança total

1. Abra o modelo de formulário no designer do InfoPath.
    
2. Clique na **guia Arquivo,** na guia **Informações,** clique em **Opções de Formulário.**
    
3. Clique na **categoria Segurança e Confiança** e des limpe a caixa de seleção Determinar automaticamente o nível **de** segurança. 
    
4. Selecione **Confiança Total**.
    
Em seguida, publique o formulário usando o procedimento a seguir, mas esteja ciente de que há algumas diferenças em relação a um procedimento de publicação padrão.
  
### <a name="to-publish-an-administrator-deployed-solution"></a>Para publicar uma solução implantada pelo administrador

1. Na primeira página do Assistente de **Publicação,** especifique o local do site do SharePoint Server 2010 ou do SharePoint Foundation 2010 e clique em **Próximo.**
    
2. O InfoPath marcará automaticamente **a caixa de seleção de** modelo de formulário aprovado pelo administrador na segunda página do assistente. Clique em **Avançar**.
    
3. A terceira página é exclusiva para cenários implantados pelo administrador. Em vez de selecionar um SharePoint Server, publique o formulário em um armazenamento local. O administrador do SharePoint carregará o arquivo desse local durante o processo de implantação do administrador.
    
4. Conclua as páginas restantes do **Assistente de Publicação.**
    

