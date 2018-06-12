---
title: Criar um suplemento COM para adicionar recursos personalizados ao InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2007, a criação de suplementos de com, InfoPath 2007, adicionando recursos personalizados, suplementos COM [InfoPath 2007]
localization_priority: Normal
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: Microsoft InfoPath oferece suporte a suplementos COM para estender o experiência do usuário de edição de formulários. Embora o suporte para suplementos COM foi adicionado pela primeira vez no InfoPath, outros aplicativos do Office, como o Microsoft Office Word e Microsoft Office Excel o oferecem suporte a suplementos COM desde o Office 2000.
ms.openlocfilehash: 4c70dfb71cf7b15a0978b4567ffac02a8ba524c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765505"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>Criar um suplemento COM para adicionar recursos personalizados ao InfoPath

Microsoft InfoPath oferece suporte a suplementos COM para estender o experiência do usuário de edição de formulários. Embora o suporte para suplementos COM foi adicionado pela primeira vez no InfoPath, outros aplicativos do Office, como o Microsoft Office Word e Microsoft Office Excel o oferecem suporte a suplementos COM desde o Office 2000.
  
Add-in COM suporte no InfoPath está disponível para o ambiente de edição de formulários. O ambiente de design do formulário não pode ser estendido usando suplementos COM.
  
## <a name="the-idtextensibility2-interface"></a>A Interface IDTExtensibility2

O InfoPath ambiente de edição oferece suporte para a interface **IDTExtensibility2** , que deve ser implementada por desenvolvedores de suplementos de COM **IDTExtensibility2** é um objeto de interface dupla que fornece cinco métodos que atuam como eventos dentro do ambiente de edição. Esses métodos permitem que o suplemento COM responder a ambiente inicialização e desligamento condições listadas na tabela a seguir. 
  
|**Interface**|**Descrição**|
|:-----|:-----|
|**OnAddInsUpdate (ByVal custom() como variante)** <br/> |Ocorre quando um suplemento for carregado ou descarregado no ambiente.  <br/> |
|**OnBeginShutdown (ByVal custom() como variante)** <br/> |Ocorre quando o ambiente está sendo desligado.  <br/> |
|**OnConnection (ByVal como objeto Application, ByVal ConnectMode como ext_ConnectMode, ByVal AddInInst como objeto, ByVal custom() como Variant)** <br/> |Ocorre quando um suplemento é carregado no ambiente.  <br/> |
|**OnDisconnection (ByVal RemoveMode como ext_DisconnectMode, ByVal custom() como Variant)** <br/> |Ocorre quando um suplemento seja descarregado do ambiente.  <br/> |
|**OnStartupComplete (ByVal custom() como variante)** <br/> |Ocorre quando o ambiente completou a inicialização.  <br/> |
   
## <a name="registering-com-add-ins"></a>Registrando suplementos COM

Todos os aplicativos do Office, incluindo o InfoPath, usam o registro aos suplementos de lista da coleção de suplementos COM, para armazenar o estado de conectar e para armazenar as informações de inicialização ou a demanda de carga. Para InfoPath suplementos COM, o nome de cada suplemento aparece na seguinte chave:
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
Para suplementos COM instalados para uso por cada usuário do computador cliente, a chave do registro está localizada no hive do registro HKLM:
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
O nome da chave do registro corresponde ao **ProgIdAttribute** do add-in e contém os seguintes valores. 
  
|**Name**|**Type**|**Descrição**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**String** <br/> |O nome que é exibido na caixa de diálogo **suplementos COM** e listado na página **Add-ins** do **Centro de confiança**.  <br/> |
|**Descrição** <br/> |**String** <br/> |A cadeia de caracteres que é exibida quando o suplemento é selecionado na **Central de confiabilidade**.  <br/> |
|**LoadBehavior** <br/> |**DWORD** <br/> |Especifica a maneira como o Add-in COM é carregado. O valor pode ser uma combinação de 0, 1, 2, 8 e 16. Consulte a tabela abaixo para obter mais informações.  <br/> |
   
O valor de **DWORD** **LoadBehavior** deve conter um valor que descreve como o Add-in COM carrega no ambiente de edição. O valor pode estar entre a tabela a seguir, ou uma combinação dos valores da tabela. Por exemplo, um Add-in COM criado no Visual Studio 2005 terá um **LoadBehavior** de "3" carregado na inicialização do aplicativo e estar conectado. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Desconectada. O suplemento mostrado como inativo na caixa de diálogo **suplementos de COM** .  <br/> |
|1  <br/> |Conectado. O suplemento mostra como ativo na caixa de diálogo **suplementos de COM** .  <br/> |
|2  <br/> |Carrega na inicialização. O suplemento é carregado e conectado quando o aplicativo host for iniciado.  <br/> |
|8  <br/> |Carrega por demanda. O suplemento é carregado e conectado quando o aplicativo host exige, por exemplo, quando um usuário clica em um botão que usa a funcionalidade do add-in.  <br/> |
|16  <br/> |Conecte-se pela primeira vez. O suplemento será carregado e conectado na primeira vez em que o usuário executa o aplicativo host após se registrar o suplemento.  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Criando um suplemento de COM gerenciado com o Visual Studio 2005 ou o Visual Studio 2008

Para criar uma gerenciada COM suplemento usando o Microsoft Visual Studio 2005 ou o Visual Studio 2008, criar um projeto de suplemento compartilhado da seguinte maneira: 
  
1. Inicie o Visual Studio.
    
2. On the **File** menu, click **New Project**.
    
3. No painel **Tipos de projeto** da caixa de diálogo **Novo projeto** , clique na pasta de **Outros tipos de projetos** e clique em **extensibilidade**.
    
4. No painel de **modelos** , clique em **Suplemento compartilhado**.
    
5. Na caixa **nome** , digite um nome para o projeto. 
    
6. Na caixa **local** , digite um caminho de pasta ou clique em **Procurar** e selecione um caminho de pasta e clique em **Okey**. O **Assistente de suplemento compartilhado** aparece. 
    
7. Clique em **Avançar** no **Assistente de suplemento compartilhado**. A página **Selecionar um idioma de programação** aparece. 
    
8. Clique em **criar um suplemento usando o Visual Basic**, clique em **Avançar**. A página **Selecionar um aplicativo Host** aparece. 
    
9. Desmarque as caixas ao lado de cada aplicativo, exceto **Microsoft InfoPath**e clique em **Avançar**. A página **Insira um nome e descrição** aparece. 
    
10. Na caixa **qual é o nome do seu suplemento** , digite o nome do seu COM Add-in. 
    
11. Na caixa **qual é a descrição do seu suplemento** , digite a descrição para o COM Add-in e clique em **Avançar**. A página **Escolher opções de suplemento** aparece. 
    
12. Verifique os **gostaria de meu suplemento carregado quando o aplicativo host for carregado** e caixas de **Meu suplemento deve estar disponível para todos os usuários do computador em que ele foi instalado, não somente a pessoa que instala a ele** . 
    
13. Clique em **próximo** para revisar a página de **Resumo** , clique em **Concluir**.
    
Depois que o projeto é criado pelo Visual Studio, você verá dois projetos na janela do Gerenciador de soluções. O primeiro projeto é o projeto para o COM Add-in; o segundo projeto é um projeto de instalação para implantar o Add-in de COM. O **Assistente de suplemento compartilhado** apenas insere uma referência para a **Biblioteca de objetos do Microsoft Office 14.0**, portanto, é necessário inserir uma referência à biblioteca de objeto do InfoPath usando as seguintes etapas:
  
1. Clique duas vezes em **Meu projeto** para exibir as propriedades do projeto de suplemento. Clique na guia **referências** para exibir as referências automaticamente adicionadas ao projeto. 
    
2. Clique no botão **Adicionar** para exibir a caixa de diálogo **Adicionar referência** . 
    
3. Na guia **COM** , clique duas vezes em **Biblioteca de tipos do Microsoft.InfoPath 2.0**e clique em **Okey**.
    
4. Adicionando uma referência à **Biblioteca de tipos do Microsoft InfoPath 3.0** também adiciona o referências a três assemblies que devem ser removidos: **ADODB**, **MSHTML**e **MSXML2**. No **Solution Explorer** sob **referências**, do mouse em cada uma dessas referências e clique em **Remover**.
    
## <a name="viewing-the-registry-settings"></a>Exibindo as configurações do registro

Para exibir as configurações do registro que serão criadas quando o COM Add-in estiver instalado, siga estas etapas:
  
1. Com o botão direito no nó raiz do projeto de instalação no **Solution Explorer**, clique em **modo de exibição**, em seguida, **Editor**, e clique em **registro**.
    
2. No painel esquerdo, clique no sinal de mais para expandir **HKEY_LOCAL_MACHINE**, **Software**, **Microsoft**, **InfoPath**e **AddIns**.
    
3. Clique no nome correspondente à compartilhado suplemento do seu projeto **ProgID**.
    
Para alterar qualquer uma dessas propriedades, clique com o botão a propriedade, clique na **Janela Propriedades**e altere a caixa de **valor** na **Janela Propriedades**.
  
## <a name="compiling-and-distributing-the-shared-add-in"></a>Compilando e distribuir o suplemento compartilhado

Para compilar o Add-in COM gerenciado para testes no computador em que o projeto de suplemento compartilhado foi desenvolvido, com o botão direito no nó raiz do projeto de suplemento compartilhado no Solution Explorer e clique em criar. Se o projeto é compilado sem erros, você pode iniciar o ambiente de edição do InfoPath e começar a usar o Add-in COM gerenciado. Se você tiver uma instância do InfoPath em execução, feche-o antes de criar o projeto. Talvez também seja necessário abrir a caixa de diálogo Suplementos COM para verificar se o Add-in COM está registrado. Para abrir a caixa de diálogo Suplementos COM, siga estas etapas:
  
1. Abra o ambiente de edição do InfoPath. A maneira mais fácil de fazer isso é abrir um modelo de formulário existente, que criará um novo formulário baseado no modelo de formulário.
    
2. No menu **Ferramentas** , clique em **Central de confiabilidade** . 
    
3. Clique na categoria de **suplementos** no lado esquerdo. 
    
4. Na seção **Gerenciar** na parte inferior da caixa de diálogo **Central de confiabilidade** , selecione **suplementos COM** na lista e clique no botão **Ir** . 
    
5. Na caixa de diálogo **suplementos COM** , você verá o nome do seu suplemento recentemente criado e deve haver uma caixa de seleção ao lado dela. Se não houver nenhuma caixa de seleção ao lado dela, o Add-in COM Falha ao carregar devido a um erro, o que será listado na seção **Carregar o comportamento** da caixa de diálogo. 
    
Para compilar o gerenciada suplemento COM para uso em um computador diferente do computador no qual o projeto de suplemento compartilhado desenvolvido, você deve seguir etapas adicionais para proteger seu código. Para obter informações sobre como proteger os projetos de suplemento compartilhado para uso em outros computadores, consulte três artigos a seguir:
  
- [Implantação de gerenciada suplementos COM no Office XP](http://go.microsoft.com/fwlink/?LinkID=73473)
  
- [Usando a solução de correção de suplemento COM para implantar gerenciado suplementos COM no Office XP](http://go.microsoft.com/fwlink/?LinkID=73474)
  
- [Isolando extensões do Office com o Assistente de correção de COM](http://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> Não isolar o Add-in COM pode causar vazamento de memória e instabilidade do aplicativo. 
  
> [!NOTE]
> Se o .NET Framework ou outros assemblies necessários do projeto de instalação não já estiverem instalados em computadores de destino, o arquivo. msi pode não ser instalado corretamente. Além disso, você não pode distribuir o arquivo. msi e, em seguida, tente instalar o arquivo. msi. Você também deve distribuir os outros arquivos de suporte na mesma pasta do arquivo. msi original gerado pelo Visual Studio. 
  
## <a name="coding-in-the-com-add-in"></a>Codificação no suplemento COM

Eventos de aplicativo que ocorrem no ambiente de edição de formulário do InfoPath podem ser capturados por um COM Add-in. Os eventos a seguir do objeto [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) podem ser usados pelo COM Add-in para responder a ações do usuário: 
  
|**Event**|**Descrição**|
|:-----|:-----|
|[NewXDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.NewXDocument.aspx) Evento  <br/> |Ocorre quando um novo formulário é criado.  <br/> |
|[Encerre](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.Quit.aspx) Evento  <br/> |Ocorre quando o usuário encerra o InfoPath.  <br/> |
|[WindowActivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowActivate.aspx) Evento  <br/> |Ocorre quando qualquer janela de documento é ativada.  <br/> |
|[WindowDeactivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowDeactivate.aspx) Evento  <br/> |Ocorre quando qualquer janela de documento é desativada.  <br/> |
|[WindowSize](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowSize.aspx) Evento  <br/> |Ocorre quando qualquer janela de documento é redimensionada ou movida.  <br/> |
|[XDocumentBeforeClose](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeClose.aspx) Evento  <br/> |Ocorre imediatamente antes de qualquer documento aberto fechar.  <br/> |
|[XDocumentBeforePrint](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforePrint.aspx) Evento  <br/> |Ocorre imediatamente antes de qualquer documento aberto seja impresso.  <br/> |
|[XDocumentBeforeSave](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeSave.aspx) Evento  <br/> |Ocorre imediatamente antes de qualquer documento aberto seja salvo.  <br/> |
|[XDocumentChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentChange.aspx) Evento  <br/> |Ocorre quando um novo formulário é criado, quando um formulário existente é aberto ou quando outro formulário é feito formulário ativo.  <br/> |
|[XDocumentOpen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentOpen.aspx) Evento  <br/> |Ocorre quando um documento é aberto.  <br/> |
   
Para capturar esses eventos na COM Add-in, você deve declarar as seguintes variáveis de nível de classe na classe **Connect** : 
  
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

A primeira linha projeta o aplicativo genérico **objeto** recebida pelo suplemento para o objeto [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx) . A segunda linha usa a propriedade de [eventos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx) do objeto **_Application3** (representado pela variável **InfoPathApplication** ) ao objeto [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) . 
  
Para criar manipuladores de eventos, selecione **InfoPathApplicationEvents** na caixa de lista suspensa de **Nome de classe** na parte superior da janela do Visual Studio e, em seguida, selecione o evento que você deseja manipular na caixa suspensa **Nome do método** na parte superior do Visual Janela Studio. Por exemplo, se você precisar controlar quando um formulário é salvo, manipular o evento **XDocumentBeforeSave** . Selecionar **XDocumentBeforeSave** na lista suspensa **Nome do método** automaticamente insere o procedimento a seguir: 
  
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

Qualquer um dos eventos do objeto **ApplicationEvents** podem ser administrados COM Add-in do usando o mesmo método. 
  
## <a name="see-also"></a>Confira também

- [Criando um Microsoft Office 2000 suplemento COM](http://go.microsoft.com/fwlink/?LinkID=73468) 
- [Criando o Office gerenciado suplementos de COM o Visual Studio .NET](http://go.microsoft.com/fwlink/?LinkID=73470)
- [Trabalhando com os procedimentos de evento IDTExtensibility2](http://go.microsoft.com/fwlink/?LinkID=73471)
- [Construir um Office suplemento COM o Visual Basic .NET](http://go.microsoft.com/fwlink/?LinkID=73469)
- [Construir um Office suplemento COM o Visual c# .NET](http://go.microsoft.com/fwlink/?LinkID=73472)
- [Criando suplementos de 2007 do InfoPath usando o Visual Studio 2005 Tools for the Office System SE](http://msdn.microsoft.com/en-us/library/bb968857%28office.12%29.aspx)

