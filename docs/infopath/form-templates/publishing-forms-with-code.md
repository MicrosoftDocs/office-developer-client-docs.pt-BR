---
title: Publicando formulários com código
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
# <a name="publishing-forms-with-code"></a>Publicando formulários com código

Qualquer administrador de conjunto de sites pode publicar formulários com código diretamente a partir do Assistente de publicação do InfoPath Designer para uma biblioteca de formulários no SharePoint. O código é executado em um ambiente de área restrita para que o código mal-intencionado não pode prejudicar o servidor. Isso é conhecido como uma solução alternativa de publicação ou publicar a infraestrutura de área restrita do SharePoint.
  
InfoPath 2010 e o SharePoint Server 2010 também suportam soluções implantados pelo administrador. Designer de formulários publica formulários com código em um repositório local que posteriormente analisado e carregados por um administrador de farm do SharePoint. O código recebe confiança total e pode incorporar funcionalidade que exija privilégios elevados como e/s do arquivo.
  
## <a name="comparing-sandboxed-and-administrator-approved-solutions"></a>Comparar as soluções de área restrita e aprovados pelo administrador

A tabela a seguir resume as diferenças entre a publicação de soluções em área restrita e aprovados pelo administrador. 
  
||**Soluções em área restrita**|**Soluções aprovados pelo administrador**|
|:-----|:-----|:-----|
|**Permissões necessárias** <br/> |Podem ser publicadas por qualquer administrador de conjunto de sites.  <br/> |Podem ser implantados por um administrador de farm.  <br/> |
|**Publicação** <br/> |Podem ser publicadas diretamente do InfoPath.  <br/> |Pode ser implantado usando a Administração Central ou a ferramenta de linha de comando stsadm.  <br/> |
|**Protection** <br/> |Código é executado em um ambiente de área restrita. Isso ajuda a proteger o servidor de código mal-intencionado.  <br/> |Código pode ser executado com confiança total e acessar qualquer recurso no servidor.  <br/> |
|**Uso recomendado** <br/> |Formulários que requerem apenas uma pequena quantidade de código.  <br/> |Formulários que contêm várias linhas de código.  <br/> |
   
### <a name="publishing-form-templates-as-sandboxed-solutions"></a>Publicação de modelos de formulário como soluções em área restrita

Publicação de um formulário com código como uma solução alternativa não é diferente de qualquer outra forma de publicação para uma biblioteca de documentos. Basta usar o Assistente de publicação como de costume e seu formulário será carregado no servidor e vai operar da área restrita.
  
Observe que não há determinadas restrições à implantação de seu formulário como uma solução em área restrita:
  
- Deve ser um formulário do InfoPath.
    
- Deve usar c# ou Visual Basic como a linguagem de programação.
    
- Não é possível enviar para conexões de dados de email.
    
- Não podem ter propriedades promovido para conexões Web Parts.
    
- Não deve ter quaisquer conexões de dados ou controles de metadados gerenciados.
    
Para permitir que administradores do conjunto de sites usar soluções em área restrita em Microsoft SharePoint Server 2010 ou um servidor que executa o Microsoft SharePoint Foundation 2010, o administrador do farm deve iniciar o serviço de código de usuário do Windows SharePoint.
  
### <a name="to-start-the-windows-sharepoint-user-code-service"></a>Para iniciar o serviço de código de usuário do Windows SharePoint

1. Abra a Administração Central.
    
2. Em **Serviços do sistema**, clique em **Gerenciar serviços no servidor**.
    
3. Inicie o **serviço de código de usuário do Microsoft SharePoint Foundation**.
    
### <a name="to-publish-a-sandboxed-solution"></a>Para publicar uma solução em área restrita

1. Abra o modelo de formulário no designer do InfoPath.
    
2. Clique na guia **arquivo** e, em seguida, clique em **SharePoint Server** , na guia **Publicar** no Backstage. 
    
3. Insira a URL do site do SharePoint para publicar e, em seguida, clique em **Avançar**. 
    
    > [!IMPORTANT]
    > Você deve ser um administrador de conjunto de sites neste site para publicar esse modelo de formulário como uma solução em área restrita. 
  
4. Selecione a **Biblioteca de formulários**e clique em **Avançar**.
    
5. Selecione **criar uma nova biblioteca de formulários**e clique em **Avançar**.
    
6. Insira o nome e as descrições para sua biblioteca de formulários e clique em **Avançar**.
    
7. Clique em **Publicar**.
    
Por exemplo, soluções que demonstram cenários que são adequados para modelos de formulário publicados como soluções em área restrita, consulte [Exemplos de soluções em área restrita](sample-sandboxed-solutions.md).
  
### <a name="publishing-form-templates-as-administrator-deployed-solutions"></a>Publicação de modelos de formulário como soluções implantados pelo administrador

Publicar o formulário como um modelo aprovado pelo administrador recomenda-se o formulário tiver várias conexões de dados, se ele requer segurança de confiança total, ou se você precisar de um modelo de todo o farm.
  
Há várias etapas que deve ser concluídas por um administrador do farm antes de uma solução implantados pelo administrador ficará disponível no SharePoint e você, como o desenvolvedor deve preparar a solução antes do administrador está envolvido.
  
Primeiro, se o seu formulário será para ser implantado como confiança total, você deve definir o nível de segurança, conforme descrito no procedimento a seguir.
  
### <a name="to-set-the-security-level-of-a-form-template-to-full-trust"></a>Para definir o nível de segurança de um modelo de formulário como confiança total

1. Abra o modelo de formulário no designer do InfoPath.
    
2. Clique na guia **arquivo** , na guia **informações** , clique em **Opções de formulário**.
    
3. Clique na categoria de **segurança e confiança** e, em seguida, desmarque a caixa de seleção **determinar automaticamente o nível de segurança** . 
    
4. Selecione a **confiança total**.
    
Em seguida, publicá-lo usando o procedimento a seguir, mas, lembre-se de que não existem algumas diferenças de um procedimento de publicação padrão.
  
### <a name="to-publish-an-administrator-deployed-solution"></a>Para publicar uma solução implantados pelo administrador

1. Na primeira página do **Assistente de publicação**, especifique o local do site do SharePoint Server 2010 ou o SharePoint Foundation 2010 e clique em **Avançar**.
    
2. InfoPath selecionará automaticamente a caixa de seleção de **modelo de formulário aprovados pelo administrador** na segunda página do assistente. Clique em **Avançar**.
    
3. A terceira página é exclusiva cenários implantados pelo administrador. Em vez de selecionar um servidor do SharePoint, publique o formulário em um repositório local. O administrador do SharePoint carregará o arquivo a partir deste local durante o processo de implantação do administrador.
    
4. Conclua as páginas restantes do **Assistente de publicação**.
    

