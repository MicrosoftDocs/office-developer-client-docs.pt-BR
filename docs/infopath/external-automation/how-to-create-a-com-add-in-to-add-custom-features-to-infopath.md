---
title: Criar um suplemento de COM para adicionar recursos personalizados ao InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2007,criar suplementos de COM,InfoPath 2007,adicionar recursos personalizados,suplementos de COM [InfoPath 2007]
localization_priority: Normal
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: O Microsoft InfoPath é compatível com suplementos de COM para ampliar a experiência do usuário ao editar formulários. Embora o suporte para suplementos de COM tenha sido adicionado primeiro ao InfoPath, outros aplicativos do Office, como o Microsoft Office Word e o Microsoft Office Excel, oferecem suporte a suplementos de COM desde o Office 2000.
ms.openlocfilehash: f8dd16b161c4ea862cf3b15e56e26a2547c1fc4c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303784"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>Criar um suplemento de COM para adicionar recursos personalizados ao InfoPath

O Microsoft InfoPath é compatível com suplementos de COM para ampliar a experiência do usuário ao editar formulários. Embora o suporte para suplementos de COM tenha sido adicionado primeiro ao InfoPath, outros aplicativos do Office, como o Microsoft Office Word e o Microsoft Office Excel, oferecem suporte a suplementos de COM desde o Office 2000.
  
No InfoPath, o suporte a suplementos de COM está disponível para o ambiente de edição de formulários. O ambiente de design de formulário não pode ser estendido usando suplementos de COM.
  
## <a name="the-idtextensibility2-interface"></a>A interface IDTExtensibility2

O ambiente de edição do InfoPath fornece suporte para a interface **IDTExtensibility2**, que deve ser implementada por desenvolvedores de suplementos de COM. A **IDTExtensibility2** é um objeto de interface dupla que proporciona cinco métodos que atuam como eventos no ambiente de edição. Esses métodos permitem que o suplemento responda às condições de inicialização e encerramento do ambiente, listadas na tabela a seguir. 
  
|**Interface**|**Descrição**|
|:-----|:-----|
|**OnAddInsUpdate (ByVal custom() As Variant)** <br/> |Ocorre quando um suplemento é carregado ou descarregado do ambiente.  <br/> |
|**OnBeginShutdown (ByVal custom() As Variant)** <br/> |Ocorre quando o ambiente está sendo encerrado.  <br/> |
|**OnConnection(ByVal Application As Object, ByVal ConnectMode As ext_ConnectMode, ByVal AddInInst As Object, ByVal custom() As Variant)** <br/> |Ocorre quando um suplemento é carregado no ambiente.  <br/> |
|**OnDisconnection (ByVal RemoveMode As ext_DisconnectMode, ByVal custom() As Variant)** <br/> |Ocorre quando um suplemento é descarregado do ambiente.  <br/> |
|**OnStartupComplete (ByVal custom() As Variant)** <br/> |Ocorre quando o ambiente conclui a inicialização.  <br/> |
   
## <a name="registering-com-add-ins"></a>Registrar suplementos de COM

Todos os aplicativos do Office, incluindo o InfoPath, usam o registro para listar suplementos na coleção de suplementos de COM, para armazenar o estado de conexão e armazenar informações sobre a inicialização ou o carregamento sob demanda. Para os suplementos de COM do InfoPath, o nome de cada suplemento é exibido na seguinte chave:
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
Para os suplementos de COM instalados para uso por todos os usuários de computadores clientes, a chave do registro está localizada na seção do registro HKLM:
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
O nome da chave do registro corresponde ao **ProgIdAttribute** do suplemento e contém os valores a seguir. 
  
|**Nome**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**Cadeia de caracteres** <br/> |O nome é exibido na caixa de diálogo **Suplementos de COM** e listado na página **Suplementos** da **Central de Confiabilidade**.  <br/> |
|**Descrição** <br/> |**Cadeia de caracteres** <br/> |A cadeia de caracteres exibida quando o suplemento é selecionado na **Central de Confiabilidade**.  <br/> |
|**LoadBehavior** <br/> |**DWORD** <br/> |Especifica a maneira de carregamento do suplemento de COM. O valor pode ser uma combinação de 0, 1, 2, 8 e 16. Consulte a tabela abaixo para saber mais.  <br/> |
   
O valor **DWORD** para **LoadBehavior** deve conter um valor que descreve como o suplemento de COM é carregado no ambiente de edição. O valor pode ser da tabela abaixo, ou uma combinação dos valores da tabela. Por exemplo, um suplemento de COM criado no Visual Studio 2005 terá o **LoadBehavior** "3" carregado na inicialização do aplicativo e estará conectado. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Desconectado. O suplemento é exibido como Inativo na caixa de diálogo **Suplemento de COM**.  <br/> |
|1   <br/> |Conectado. O suplemento é exibido como Ativo na caixa de diálogo **Suplemento de COM**.  <br/> |
|2   <br/> |Carrega na Inicialização. O suplemento é carregado e conectado quando o aplicativo host inicia.  <br/> |
|8   <br/> |Carrega por Demanda. O suplemento é carregado e conectado quando o aplicativo host exige, por exemplo, quando um usuário clica em um botão que utiliza a funcionalidade do suplemento.  <br/> |
|16   <br/> |Conectar na primeira vez. O suplemento será carregado e conectado na primeira vez que o usuário executar o aplicativo host após registrar o suplemento.  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Criar um suplemento de COM gerenciado com o Visual Studio 2005 ou Visual Studio 2008

Para criar um suplemento de COM gerenciado usando o Microsoft Visual Studio 2005 ou Visual Studio 2008, crie um projeto de suplemento compartilhado da seguinte maneira: 
  
1. Inicie o Visual Studio.
    
2. No menu **Arquivo**, clique em **Novo Projeto**.
    
3. No painel **Tipos de projeto** da caixa de diálogo **Novo Projeto**, clique na pasta **Outros tipos de projeto** e em **Extensibilidade**.
    
4. No painel **Modelos**, clique em **Suplemento compartilhado**.
    
5. Na caixa **Nome**, digite um nome para o projeto.  
    
6. Na caixa **Local**, digite o caminho da pasta ou clique em **Procurar**, selecione um caminho de pasta e clique em **OK**. O **Assistente de Suplemento Compartilhado** é exibido. 
    
7. Clique em **Avançar** no **Assistente de Suplemento Compartilhado**. A página **Selecione uma Linguagem de Programação** é exibida. 
    
8. Clique em **Criar Suplemento usando o Visual Basic** e em **Avançar**. A página **Selecione um Aplicativo Host** é exibida. 
    
9. Desmarque as caixas ao lado de cada aplicativo, exceto por **Microsoft InfoPath** e clique em **Avançar**. A página **Digite um Nome e uma Descrição** é exibida. 
    
10. Na caixa **Qual o nome do seu Suplemento**, digite o nome do seu suplemento de COM. 
    
11. Na caixa **Qual é a descrição do seu Suplemento**, digite a descrição de seu Suplemento de COM e clique em **Avançar**. A página **Escolha Opções de Suplemento** é exibida. 
    
12. Marque as caixas **Eu quero que meu suplemento carregue quando o aplicativo host carregar** e **Meu suplemento deve estar disponível para todos os usuários do computador em que foi instalado e não apenas para a pessoa que instalá-lo**. 
    
13. Clique em **Avançar** para revisar a página **Resumo** e, depois, clique em **Concluir**.
    
Depois do projeto ser criado pelo Visual Studio, você verá dois projetos na janela Gerenciador de Soluções. O primeiro é do Suplemento de COM; o segundo é um projeto de configuração para a implantação do Suplemento de COM. O **Assistente de Suplemento Compartilhado** insere somente uma referência para a **Biblioteca de Objetos do Microsoft Office 14.0**, portanto, é necessário inserir uma referência na biblioteca de objetos do InfoPath usando as etapas a seguir:
  
1. Clique duas vezes em **Meu Projeto** para exibir as propriedades do projeto de suplemento. Clique na guia **Referências** para exibir as referências adicionadas automaticamente ao projeto. 
    
2. Clique no botão **Adicionar** para exibir a caixa de diálogo **Adicionar Referência**. 
    
3. Na guia **COM**, clique duas vezes em **Biblioteca de Tipos do Microsoft InfoPath 2.0** e clique em **OK**.
    
4. Adicionar uma referência à **Biblioteca de Tipos do Microsoft InfoPath 3.0** também adiciona as referências a três assemblies que devem ser removidos: **ADODB**, **MSHTML** e **MSXML2**. No **Gerenciador de Soluções**, em **Referências**, clique com o botão direito do mouse em cada uma dessas referências e, depois, clique em **Remover**.
    
## <a name="viewing-the-registry-settings"></a>Exibir as configurações de registro

Para exibir as configurações de registro que serão criadas quando o suplemento de COM for instalado, siga estas etapas:
  
1. Clique com o botão direito do mouse no nó raiz do projeto de instalação em **Gerenciador de Soluções**, depois clique em **Exibir**, em **Editor** e em **Registro**.
    
2. No painel à esquerda, clique no sinal de mais para expandir **HKEY_LOCAL_MACHINE**, **Software**, **Microsoft**, **InfoPath** e **Suplementos**.
    
3. Clique no nome correspondente à **ProgID** do seu projeto de suplemento compartilhado.
    
Para alterar uma dessas propriedades, clique com o botão direito do mouse na propriedade, clique em **Janela de Propriedades** e altere a caixa **Valor** na **Janela de Propriedades**.
  
## <a name="compiling-and-distributing-the-shared-add-in"></a>Compilar e distribuir o suplemento compartilhado

Para compilar o suplemento de COM gerenciado para teste no computador em que o projeto do suplemento compartilhado foi desenvolvido, clique com o botão direito do mouse no nó raiz do projeto do suplemento compartilhado no Gerenciador de Soluções, depois clique em Compilar. Se o build do projeto não tiver erros, você pode iniciar o ambiente de edição do InfoPath e começar a usar o suplemento de COM gerenciado. Se houver uma instância do InfoPath em execução, feche-a antes de criar o projeto. Também pode ser necessário abrir a caixa de diálogo Suplementos de COM para verificar se o suplemento de COM está registrado. Para abrir a caixa de diálogo Suplementos de COM, siga estas etapas:
  
1. Abra o ambiente de edição do InfoPath. Para isso, a maneira mais fácil é abrir um modelo de formulário existente, que cria um novo formulário baseado nesse modelo.
    
2. Clique em **Central de Confiabilidade** no menu **Ferramentas**. 
    
3. Clique na categoria **Suplementos** à esquerda. 
    
4. Na seção **Gerenciar** da parte inferior da caixa de diálogo **Central de Confiabilidade**, selecione **Suplementos de COM** na lista e clique no botão **Ir**. 
    
5. Na caixa de diálogo **Suplementos de COM**, você verá o nome do seu suplemento recentemente criado e haverá uma caixa de seleção ao lado. Se não houver nenhuma caixa de seleção ao lado, houve falha no carregamento do Suplemento de COM devido a um erro que será listado na seção **Comportamento do carregamento** da caixa de diálogo. 
    
Para compilar o suplemento de COM gerenciado para uso em um computador diferente daquele no qual o projeto do suplemento compartilhado foi desenvolvido, você deve seguir etapas adicionais para proteger o código. Para saber mais sobre a proteção de projetos de Suplemento Compartilhado para uso em outros computadores, consulte os três artigos a seguir:
  
- [Implantar suplementos de COM gerenciados no Office XP](https://go.microsoft.com/fwlink/?LinkID=73473)
  
- [Usar a solução de correção de suplementos de COM para implantar suplementos de COM gerenciados no Office XP](https://go.microsoft.com/fwlink/?LinkID=73474)
  
- [Isolar extensões do Office com o assistente de correção de COM](https://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> Não isolar o suplemento de COM pode causar perdas de memória e instabilidade no aplicativo. 
  
> [!NOTE]
> Se o .NET Framework ou outros assemblies necessários para a configuração do projeto ainda não estiverem instalados nos computadores de destino, o arquivo .msi pode não ser instalado corretamente. Além disso, você não pode distribuir o arquivo .msi e depois tentar instalá-lo. Você também deve distribuir outros arquivos de suporte na mesma pasta do arquivo .msi original gerado pelo Visual Studio. 
  
## <a name="coding-in-the-com-add-in"></a>Codificação do suplemento de COM

Os eventos de aplicativos que ocorrem no ambiente de edição de formulários do InfoPath podem ser capturados por um Suplemento de COM. Os seguintes eventos do objeto [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) podem ser usados pelo Suplemento de COM para responder a ações de usuário: 
  
|**Evento**|**Descrição**|
|:-----|:-----|
|Evento [NewXDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.NewXDocument.aspx)  <br/> |Ocorre quando um novo formulário é criado.  <br/> |
|Evento [Quit](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.Quit.aspx)  <br/> |Ocorre quando o usuário encerra o InfoPath.  <br/> |
|Evento [WindowActivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowActivate.aspx)  <br/> |Ocorre quando qualquer janela de documento é ativada.  <br/> |
|Evento [WindowDeactivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowDeactivate.aspx)  <br/> |Ocorre quando qualquer janela de documento é desativada.  <br/> |
|Evento [WindowSize](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowSize.aspx)  <br/> |Ocorre quando qualquer janela de documento é redimensionada ou movida.  <br/> |
|Evento [XDocumentBeforeClose](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeClose.aspx)  <br/> |Ocorre imediatamente antes que qualquer documento aberto seja fechado.  <br/> |
|Evento [XDocumentBeforePrint](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforePrint.aspx)  <br/> |Ocorre imediatamente antes que qualquer documento aberto seja impresso.  <br/> |
|Evento [XDocumentBeforeSave](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeSave.aspx)  <br/> |Ocorre imediatamente antes que qualquer documento aberto seja salvo.  <br/> |
|Evento [XDocumentChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentChange.aspx)  <br/> |Ocorre quando um novo formulário é criado, quando um formulário existente é aberto ou quando um outro formulário torna-se o formulário ativo.  <br/> |
|Evento [XDocumentOpen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentOpen.aspx)  <br/> |Ocorre quando um documento é aberto.  <br/> |
   
Para capturar esses eventos no Suplemento de COM, é necessário declarar as seguintes variáveis de nível de classe em sua classe **Connect**: 
  
```vb
InfoPathApplication = DirectCast( _
   application, Microsoft.Office.Interop.InfoPath._Application3)
InfoPathApplicationEvents = DirectCast( _
   InfoPathApplication.Events, _
   Microsoft.Office.Interop.InfoPath.ApplicationEvents)
```

```cs
InfoPathApplication =
   (Microsoft.Office.Interop.InfoPath._Application3)application;
InfoPathApplicationEvents =
   (Microsoft.Office.Interop.InfoPath.ApplicationEvents)
   InfoPathApplication.Events;
```

A primeira linha projeta o **Object** do aplicativo genérico recebido pelo suplemento para o objeto [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx). A segunda linha projeta a propriedade [Eventos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx) do objeto **_Application3** (representado pela variável **InfoPathApplication**) para o objeto [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx). 
  
Para criar os manipuladores de eventos, selecione **InfoPathApplicationEvents** na caixa suspensa **Nome da classe** na parte superior da janela do Visual Studio e, em seguida, selecione o evento que você deseja manipular na caixa suspensa **Nome do método** na parte superior da janela do Visual Studio. Por exemplo, se for necessário controlar quando um formulário é salvo, manipule o evento **XDocumentBeforeSave**. Selecionar **XDocumentBeforeSave** na lista suspensa **Nome do método** insere automaticamente o procedimento a seguir: 
  
```vb
Private Sub InfoPathApplicationEvents_XDocumentBeforeSave( _
   ByVal pDocument As Microsoft.Office.Interop.InfoPath._XDocument, _
   ByRef pfCancel As Boolean) _
   Handles InfoPathApplicationEvents.XDocumentBeforeSave
End Sub
```

```cs
private void InfoPathApplicationEvents_XDocumentBeforeSave(
   Microsoft.Office.Interop.InfoPath._XDocument pDocument, ref bool pfCancel)
{
}

```

É possível manipular qualquer um dos eventos do objeto **ApplicationEvents** pelo Suplemento de COM usando o mesmo método. 
  
## <a name="see-also"></a>Confira também

- [Criar um suplemento de COM do Microsoft Office 2000](https://go.microsoft.com/fwlink/?LinkID=73468) 
- [Criar suplementos de COM gerenciados do Office com o Visual Studio .NET](https://go.microsoft.com/fwlink/?LinkID=73470)
- [Trabalhar com os procedimentos de evento IDTExtensibility2](https://go.microsoft.com/fwlink/?LinkID=73471)
- [Criar um suplemento de COM do Office com o Visual Basic .NET](https://go.microsoft.com/fwlink/?LinkID=73469)
- [Criar um suplemento de COM do Office usando o Visual C# .NET](https://support.microsoft.com/en-us/help/302901/how-to-build-an-office-com-add-in-by-using-visual-c-net)
- [Criar suplementos do InfoPath 2007 usando as ferramentas do Visual Studio 2005 para o Office System SE](https://msdn.microsoft.com/library/bb968857%28office.12%29.aspx)

