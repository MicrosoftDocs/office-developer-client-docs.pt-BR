---
title: Compreender formulários totalmente confiáveis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 64d62990-6275-edef-c639-b6ba8d10c38c
description: InfoPath fornece a capacidade de criar formulários totalmente confiáveis, que são formulários com mais permissões de segurança e que podem acessar outros recursos do sistema e outros componentes no computador de um usuário. Este artigo descreve o que é um formulário totalmente confiável e por que ele é usado, e também como criar um formulário totalmente confiável convertendo manualmente e registrando um formulário padrão, ou então assinando digitalmente um formulário padrão.
ms.openlocfilehash: 04560e0c844d6a6ff681fd366ca7da2e4db36ba1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299756"
---
# <a name="understanding-fully-trusted-forms"></a>Compreender formulários totalmente confiáveis

InfoPath fornece a capacidade de criar formulários totalmente confiáveis, que são formulários com mais permissões de segurança e que podem acessar outros recursos do sistema e outros componentes no computador de um usuário. Este artigo descreve o que é um formulário totalmente confiável e por que ele é usado, e também como criar um formulário totalmente confiável convertendo manualmente e registrando um formulário padrão, ou então assinando digitalmente um formulário padrão.

Os modelos de formulário do InfoPath podem ser implantados com níveis variáveis de segurança. O nível que você usa é determinado pelo nível de acesso a recursos externos que você deseja que o formulário tenha. Por padrão, os modelos de formulário do InfoPath têm permissão para acessar recursos do sistema e não têm permissão para usar os componentes de software que não são marcados como confiáveis quanto a scripts. No entanto, esse comportamento pode ser substituído para que um formulário possa acessar recursos do sistema e outros recursos externos, incluindo componentes de software que não são marcados como confiáveis quanto a scripts.
  
Para que um formulário seja usado, o InfoPath deve ser capaz de acessar o modelo de formulário em que o formulário se baseia. Quando você cria um modelo de formulário, o InfoPath cria uma entrada no arquivo de definição de formulário (.xsf) que contém a URL da localização do modelo de formulário. Um formulário baseado em URL é denominado como *de área restrita*. Quando um usuário o preencher, o formulário será adicionado a um cache local e seu acesso a recursos do sistema será negado. Esse tipo de formulário herda suas permissões do domínio no qual é aberto. 
  
No entanto, você pode modificar um formulário para que ele seja baseado em um Nome de recurso Uniforme (URN), que permite acesso aos recursos do sistema. Os formulários desse tipo são considerados *totalmente confiáveis*. 
  
## <a name="why-use-a-fully-trusted-form"></a>Por que usar um Formulário Totalmente Confiável?

Os formulários totalmente confiáveis têm um melhor conjunto de permissões do que os formulários de área restrita. Por exemplo, podem conter o código de programação que usa objetos externos para acessar recursos do sistema, podem usar componentes de software ou os controles do Microsoft ActiveX não marcados como confiáveis para scripts, e podem usar a lógica de negócios personalizados fornecida pelas assemblies do .NET.
  
Além disso, alguns membros do modelo de objeto do InfoPath estão definidos para o nível de segurança 3, o que significa que só podem ser usados em um formulário totalmente confiável. Por exemplo, para acessar o objeto **CommandBars** do Microsoft Office, você usa a propriedade [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) da classe [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) do InfoPath para definir uma referência para ele. Como esta propriedade está configurada com o nível de segurança 3, ela não pode ser usada em um formulário que não é totalmente confiável. 
  
> [!NOTE]
> O uso da propriedade [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) da classe [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx), ou qualquer outro membro de modelo de objeto com nível de segurança 3, em um formulário que não seja totalmente confiável resultará em um erro de “permissão negada”. 
  
## <a name="what-makes-a-form-fully-trusted"></a>O que torna um formulário totalmente confiável?

As seguintes ações, que estão envolvidas tanto na interface do usuário do InfoPath quanto nos arquivos de formulário, são requeridas para criar e usar um formulário totalmente confiável:
  
- Habilitar o InfoPath para permitir o uso de formulários totalmente confiáveis na categoria **Editores Confiáveis** da caixa de diálogo **Central de Confiabilidade**. Esta opção deve ser habilitada para que os usuários abram formulários totalmente confiáveis. 
    
- Registrar o formulário totalmente confiável no computador de destino usando o método **RegisterSolution** do objeto **Application** do InfoPath. 
    
## <a name="creating-a-fully-trusted-form"></a>Criar um Formulário Totalmente Confiável

- Você pode criar o formulário manualmente, o que envolve modificar diretamente alguns arquivos de formulário.
    
- Você pode assinar digitalmente o modelo de formulário.
    
### <a name="manually-creating-a-fully-trusted-form"></a>Criar um Formulário Totalmente Confiável manualmente

#### <a name="to-manually-create-a-fully-trusted-form"></a>Para criar manualmente um formulário totalmente confiável

1. Fazer uma cópia de backup do modelo de formulário que você deseja tornar totalmente confiável.
    
2. Abra o modelo de formulário no InfoPath.
    
3. Salve os arquivos de origem dos formulários em uma pasta em seu disco rígido, clicando na guia **Arquivo**, clicando em **Publicar** e depois em **Exportar arquivos de origem**.
    
4. Especifique a pasta onde deseja salvar os arquivos de origem dos formulários, clique em **OK** e saia do InfoPath Designer.
    
5. Na pasta onde os arquivos de formulário foram extraídos, abra o arquivo de definição de formulário (.xsf), nomeado `manifest.xsf` por padrão, em um editor de texto como o Microsoft Notepad. 
    
6. Adicione os atributos de seguir ao elemento **xDocumentClass** no arquivo. xsf: 
   
   `requireFullTrust="yes"`<br/>
   `name="urn:MyForm:MyCompany`

   > [!NOTE]
   > Os valores que são usados para a URN podem ser qualquer tipo de valor de cadeia de caracteres, desde que esse valor seja único. Deve haver pelo menos dois valores após o prefixo `urn:`, e esses valores devem ser separados por um ponto-e-vírgula. Além disso, a URN não deve exceder 255 caracteres. 
  
7. Salve e feche o arquivo. xsf e depois abra o arquivo do modelo XML (.xml), que é nomeado `Template.xml` por padrão, em um editor de texto como o Notepad. 
    
8. Remova o atributo **href** da instrução de processamento `mso-infoPathSolution` e substitua-o pelo mesmo atributo **name** que você usou na etapa 6 para o arquivo .xsf. 
    
   > [!NOTE]
   > Os valores URN usados para o atributo **name** devem ser os mesmos no arquivo .xsf e no arquivo do modelo XML. 
  
9. Salve e feche o arquivo de modelo XML.
    
10. Reempacote os arquivos em um formato CAB .xsn com uma ferramenta como makecab.exe.
    
    > [!NOTE]
    > Embora o designer de formulários do InfoPath suporte o reempacotamento de arquivos de formulário em um arquivo .xsn existente, essa ação reverte o formulário para um formulário baseado em URL. Por esse motivo, você deve reempacotar os arquivos manualmente para evitar substituir suas alterações nos arquivos de formulário. 
  
11. Crie uma programa de instalação personalizado usando o método **RegisterSolution** do objeto **Application** do InfoPath para instalar o formulário totalmente confiável. Uma maneira simples de fazer isso é criar um arquivo de script que usa as linhas seguintes de código (na sintaxe Microsoft JScript ou VBScript): 
    
    ```js
        objIPApp = new ActiveXObject("InfoPath.Application"); 
        objIPApp.RegisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
        objIPApp.Quit(); 
        objIPApp = null;
    ```
   
    ```vb
        Public Sub InstallForm()
            Dim objIPApp As Object
            ' Create a reference to the Application object.
            Set objIPApp = CreateObject("InfoPath.Application")
            ' Register the InfoPath form template.
            objIPApp.RegisterSolution ("C:\\My Forms\\MyFormTemplate.xsn")
            MsgBox "The InfoPath form template has been registered."
            Set objIPApp = Nothing
        End Sub
        
    ```

> [!NOTE] 
> Embora este exemplo use um arquivo de script simples, você também pode usar um mecanismo de instalação mais robusto como arquivos Microsoft Windows Installer (.msi). Certifique-se, no entanto, de usar o método **RegisterSolution** para instalar corretamente o formulário totalmente confiável no computador de destino. Para acessar o método **RegisterSolution** do objeto **Application** do InfoPath a partir do Visual Basic ou do Visual Studio, defina uma referência na biblioteca de tipos do Microsoft InfoPath 3.0, que é fornecida pelo IPEDITOR.dll instalado em C:\Arquivos de Programas\Microsoft Office\Office14. 
  
Se você precisar remover um formulário totalmente confiável, pode usar o método **UnregisterSolution** do objeto **Application**, como mostrado nos seguintes exemplos de JScript e VBScript. 
    
```js
    objIPApp = new ActiveXObject("InfoPath.Application"); 
    objIPApp.UnregisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
    objIPApp.Quit(); 
    objIPApp = null;
```

```vb
    Public Sub UninstallForm()
        Dim objIPApp As Object
        ' Create a reference to the Application object.
        Set objIPApp = CreateObject("InfoPath.Application")
        ' Unregister the InfoPath form template.
        objIPApp.UnregisterSolution ("C:\My Forms\MyFormTemplate.xsn")
        MsgBox ("The InfoPath form template has been unregistered.")
        Set objIPApp = Nothing
    End Sub
    
```

### <a name="digitally-signing-a-form-template-to-create-a-fully-trusted-form"></a>Assinar digitalmente um modelo de formulário para criar um formulário totalmente confiável

Assinar digitalmente um modelo de formulário permite que você implante um modelo de formulário totalmente confiável por email ou em um servidor Web, como um servidor executando o Microsoft SharePoint Foundation. Use as etapas dos três procedimentos seguintes para fazer um formulário totalmente confiável especificando confiabilidade total para o formulário, assinando-o digitalmente e depois publicando-o.
  
#### <a name="to-digitally-sign-a-form-template"></a>Para assinar digitalmente um modelo de formulário

1. Abra o formulário no designer do InfoPath, clique na guia **Arquivo** e, em seguida, em **Opções de Formulário** na guia **Informações**. 
    
2. Na caixa de diálogo **Opções de Formulário**, clique na categoria **Segurança e Confiabilidade**. 
    
3. Desmarque a caixa de seleção **Determinar automaticamente o nível de segurança (recomendado)**.
    
4. Selecione **Confiabilidade Total (o formulário tem acesso a arquivos e configurações do computador do usuário)**.
    
5. Em **Assinatura do Modelo de Formulário**, selecione **Assinar este modelo de formulário**.
    
6. Clique em **Selecionar Certificado** para selecionar um certificado foi baixado e instalado anteriormente de um provedor de certificação confiável. 
    
7. Clique duas vezes em OK para sair totalmente.
    
#### <a name="to-publish-the-form-template-to-a-sharepoint-document-library"></a>Para publicar o modelo de formulário em uma biblioteca de documentos do SharePoint

1. Clique na guia **Arquivo**, clique em **Publicar** e em **SharePoint Server**.
    
2. Siga as instruções do**Assistente de publicação** para publicar o modelo de formulário em uma biblioteca de documentos nova ou existente do SharePoint. 
    
#### <a name="to-a-create-a-form-that-is-based-on-your-fully-trusted-digitally-signed-form-template"></a>Para criar um formulário baseado no modelo de formulário totalmente confiável assinado digitalmente

1. Na biblioteca de documentos do SharePoint, clique em **Preencher o formulário**.
    
   > [!NOTE]
   > Depois de publicar o modelo de formulário para uma biblioteca de documentos do SharePoint usando o **Assistente de publicação**, o modelo não será exibido como um item na biblioteca de formulários. Quando você cria um formulário nessa biblioteca de documentos, o modelo será usado por padrão como o modelo para o novo formulário. 
  
2. Se o modelo de formulário padrão foi assinado digitalmente, o InfoPath exibe um aviso de segurança sobre o modelo de formulário assinado digitalmente. Selecione **Sempre confiar em arquivos deste editor e abri-los automaticamente**e, em seguida, clique em **Abrir**.
    
## <a name="using-a-fully-trusted-form"></a>Usar um formulário totalmente confiável

Usar um formulário totalmente confiável é muito semelhante a usar um formulário padrão. As únicas diferenças significativas são que o formulário pode acessar recursos restritos e que avisos não serão mais exibidos.
  
> [!NOTE]
> Para habilitar o InfoPath a usar um formulário totalmente confiável, os usuários devem garantir que a caixa de seleção **Permitir a execução de formulários totalmente confiáveis em meu computador** esteja selecionada na categoria **Editores Confiáveis** da caixa de diálogo **Central de Confiabilidade**. Para abrir a caixa de diálogo **Central de Confiabilidade**, clique na guia **Arquivo**, clique em **Opções** (abaixo da guia **InfoPath**), clique em **Central de Confiabilidade** e depois em **Configurações da Central de Confiabilidade**. 
  
Um formulário totalmente confiável pode ser aberto no InfoPath a partir da caixa de diálogo **Preencher um formulário**. 
  
A caixa de diálogo **Preencher um formulário** se abre quando você clica em **Mais Formulários** no painel de tarefas **Preencher um formulário**, ou quando você clica em **Preencher um formulário** no menu **Arquivo**. 
  
### <a name="making-changes-to-a-fully-trusted-form"></a>Fazer alterações em um formulário totalmente confiável

Se você precisar fazer alterações apenas em um arquivo .xsn, pode fazer com que os usuários substituam seu arquivo .xsn existente pelo novo arquivo depois que as alterações forem feitas. Eles não precisarão reinstalá-lo usando um programa de instalação personalizado.
  
Porém, se você estiver fazendo alterações em arquivos de formulário que o arquivo .xsn contém, vai precisar reempacotar os arquivos, como explicado anteriormente, e depois fazer com que os usuários reinstalem o formulário totalmente confiável.
  
> [!NOTE]
> A melhor abordagem é salvar o modelo de formulário de volta no formato .xsn do designer do InfoPath e depois seguir as etapas deste artigo para criar um formulário totalmente confiável. 
  
## <a name="conclusion"></a>Conclusão

Dependendo dos requisitos de seu negócio e das necessidades dos seus usuários, você pode precisar criar um formulário com um conjunto de permissões mais elevado do que o formulário padrão do InfoPath. O InfoPath proporciona a capacidade de modificar um formulário de forma que ele possa acessar recursos do sistema e outros recursos externos não marcados como confiáveis quanto a script. Isso pode ser feito manualmente, fazendo modificações nos arquivos de formulário que um modelo de formulário contém e executando um script de instalação, ou então assinando digitalmente o modelo de formulário.
  

