---
title: Exemplo de soluções em modo seguro
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 415fa0fa-b7b7-4acb-a437-f54c34064004
description: Este tópico fornece dois exemplos que mostram o tipo de código que você pode escrever em uma solução em áreas de segurança do InfoPath e como publicar o modelo de formulário.
ms.openlocfilehash: 56a9a2a765100ef327790265c7cf734903268bed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439335"
---
# <a name="sample-sandboxed-solutions"></a>Exemplo de soluções em modo seguro

Os formulários do InfoPath com código gerenciado podem ser publicados na infraestrutura de soluções em áreas alternativas do SharePoint do InfoPath Designer. Este tópico fornece dois exemplos que mostram o tipo de código que você pode escrever em uma solução em áreas de segurança do InfoPath e como publicar o modelo de formulário.
  
## <a name="example-1-sorting-data-in-an-order-form"></a>Exemplo 1: Classificar dados em um formulário de pedido

Uma tarefa útil que você pode executar usando código em um formulário do InfoPath é classificar dados em uma tabela de repetição. Para fazer isso, o código reordena os nós no documento XML subjacente que é exibido no formulário do InfoPath. Embora o cenário descrito neste tópico seja direcionado para publicação diretamente do InfoPath como uma solução em áreas de segurança, ele também pode ser implantado como um modelo de formulário aprovado pelo administrador.
  
Antes de começar, certifique-se de que você está de acordo com os requisitos a seguir.
  
- Você é um administrador de conjunto de sites no site do SharePoint Server 2010 ou do SharePoint Foundation 2010 em que deseja publicar o formulário.
    
- Verifique com o administrador do farm se o Serviço de Código em Área Segura do Microsoft SharePoint Foundation está em execução no servidor. Para obter mais informações, [consulte Formulários de Publicação com Código.](publishing-forms-with-code.md)
    
- A linguagem de programação que você selecionou para o modelo de formulário é **C#** ou **Visual Basic** sem qualquer nome de versão anterior depois dela. As versões compatíveis com o InfoPath 2007 e compatíveis com o InfoPath 2003 das linguagens de programação e modelos de objeto não têm suporte para soluções em áreas alternativas. Para obter mais informações sobre como especificar a linguagem de programação, consulte [Desenvolver com o Visual Studio.](how-to-develop-with-visual-studio.md)
    
Execute as etapas a seguir para criar um modelo de formulário que classifica os dados em um **controle tabela** de repetição no formulário. 
  
### <a name="to-create-a-form-template-that-programmatically-sorts-data-in-the-form"></a>Para criar um modelo de formulário que classifica programaticamente os dados no formulário

1. Crie um novo modelo de formulário no designer do InfoPath e adicione um **controle De tabela** de repetição ao formulário. O código de exemplo para este exemplo classifica as linhas com base na primeira coluna da tabela, mas você pode modificar facilmente o código para trabalhar com qualquer coluna. 
    
2. Adicione um **controle Button** ao formulário. O código para classificar a tabela será adicionado ao manipulador de eventos para o evento **Clicked** do botão, mas você também pode usar outro evento para essa finalidade. 
    
3. Selecione o botão, clique na guia **Propriedades** e clique em **Código Personalizado.** Se o formulário ainda não tiver sido salvo, você será solicitado a salvá-lo e, em seguida, o Editor de Código abrirá com o cursor no manipulador de eventos do botão.
    
4. Colar o código a seguir no manipulador de eventos do botão. O código coloca os elementos da primeira coluna em uma matriz, classifica a matriz e reordena a tabela com base na matriz ordenada. Este código assume que os dados que estão sendo organizados são dados de cadeia de caracteres.
    
   ```cs
    // Put the elements from the first column into an array.
    XPathNavigator root = this.CreateNavigator();
        
    // Create a node iterator which contains only the values that you want to sort.
    // For this form, the entire table is in "group1", each row is a "group2"
    // and the rows are "field1", "field2" and "field3" respectively.
    XPathNodeIterator nodeIterator = root.Select(
        "/my:myFields/my:group1/my:group2/my:field1", this.NamespaceManager);
        
    // Create arrays to use for sorting.
    string[] sortArrayWords = new string[nodeIterator.Count + 1];
    int[] sortArrayKeys = new int[nodeIterator.Count + 1];
    int arrayPosition = 1;
        
    // Populate the arrays for sorting.
    while (nodeIterator.MoveNext()) 
    {
        // Loop until there are no more elements
        sortArrayWords[arrayPosition] = nodeIterator.Current.Value;
        sortArrayKeys[arrayPosition] = arrayPosition;
        arrayPosition += 1;
    }
        
    // Sort the array.
    Array.Sort(sortArrayWords, sortArrayKeys);
    arrayPosition = 0;
        
    // Create new XML to update the table.
    string newTableXML = "";
    // Iterate through the sorted array of keys.
    for (int i = 1; i <= sortArrayWords.Length - 1; i++) 
    {
        nodeIterator = root.Select(
            "/my:myFields/my:group1/my:group2", this.NamespaceManager);
            
        // Go to the right position in the table.
        for (int j = 1; j <= sortArrayKeys[i]; j++) 
        {
            nodeIterator.MoveNext();
        }
            
        // Add the row to the XML.
        newTableXML += nodeIterator.Current.OuterXml;
    }
        
    // Set the table to use the new XML.
    root.SelectSingleNode(
        "/my:myFields/my:group1", this.NamespaceManager).InnerXml = newTableXML;
    
   ```

   ```vb
    ' Put the elements from the first column into an array.
    Dim root As XPathNavigator = Me.CreateNavigator
    ' Create a node iterator which contains only the values that you want to sort
    ' For this form, the entire table is in "group1",
    ' each row is a "group2"
    ' and the rows are "field1", "field2" and "field3" respectively.
    Dim nodeIterator As XPathNodeIterator = root.Select( _
        "/my:myFields/my:group1/my:group2/my:field1", Me.NamespaceManager)
    ' Create arrays to use for sorting.
    Dim sortArrayWords(nodeIterator.Count) As String
    Dim sortArrayKeys(nodeIterator.Count) As Integer
    Dim arrayPosition As Integer = 1
    ' Populate the arrays for sorting.
    While nodeIterator.MoveNext() ' Loop until there are no more elements
        sortArrayWords(arrayPosition) = nodeIterator.Current.Value
        sortArrayKeys(arrayPosition) = arrayPosition
        arrayPosition += 1
    End While
    ' Sort the array.
    Array.Sort(sortArrayWords, sortArrayKeys)
    arrayPosition = 0
    ' Create new XML to update the table.
    Dim newTableXML As String = ""
    ' Iterate through the sorted array of keys.
    For i As Integer = 1 To sortArrayWords.Length - 1
        nodeIterator = root.Select( _
            "/my:myFields/my:group1/my:group2", Me.NamespaceManager)
        ' Go to the right position in the table.
        For j As Integer = 1 To sortArrayKeys(i)
        nodeIterator.MoveNext()
        Next
    ' Add the row to the XML.
    newTableXML &amp;= nodeIterator.Current.OuterXml
    Next
    ' Set the table to use the new XML.
    root.SelectSingleNode("/my:myFields/my:group1", _
        Me.NamespaceManager).InnerXml = newTableXML
   ```

5. Publique seu formulário usando as seguintes etapas:
    
    1. Clique **em SharePoint Server** na guia **Publicar** no Backstage. 
        
    2. Insira a URL do site do SharePoint para publicar e clique em **Próximo.** 
        
       > [!IMPORTANT]
       > Você deve ser um administrador de conjunto de sites neste site para publicar esse modelo de formulário como uma solução em áreas de segurança. 
    
    3. Selecione **a Biblioteca de** Formulário e clique em **Próximo.**
        
    4. Selecione **Criar uma nova biblioteca de formulário** e clique em **Próximo.**
        
    5. Insira o nome e as descrições da biblioteca de formulário e clique em **Próximo.**
        
    6. Clique em **Publicar**.
    
## <a name="example-2-managing-vendors-in-a-sharepoint-list"></a>Exemplo 2: Gerenciando fornecedores em uma lista do SharePoint

Este exemplo envolve a programação no modelo de objeto do Microsoft SharePoint Foundation 2010. Para fazer isso, você deve estabelecer uma referência ao assembly Microsoft.SharePoint.dll que é instalado com uma cópia licenciada do SharePoint Server 2010.
  
Microsoft.SharePoint.Server.dll é instalado em C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI por padrão. Essa DLL deve ser incluída em projetos nos quais você programa em relação ao modelo de objeto do SharePoint. Para estabelecer uma referência à Microsoft.SharePoint.dll em um projeto do Visual Studio 2012, abra o **Editor** de Código e clique em Adicionar Referência no **menu** Ferramentas.  Na caixa **de diálogo** Adicionar  Referência, clique na guia Procurar, especifique o local do arquivo Microsoft.SharePoint.dll e clique em **OK.** Isso copiará o Microsoft.SharePoint.dll para o diretório do projeto para que você possa usar os membros do modelo de objeto do SharePoint Foundation 2010 em sua solução do InfoPath.
  
### <a name="designing-the-form-and-developing-the-code"></a>Projetando o formulário e desenvolvendo o código

No código em um formulário do InfoPath, você pode usar o modelo de objeto do SharePoint para criar itens em listas de análise. Isso é útil quando você preenche uma caixa de lista lista de uma lista do SharePoint e deseja adicionar novos valores a ela sem criar um formulário separado. Este exemplo usa uma caixa de combinação para mostrar todos os valores atualmente na lista e cria lógica de programação para adicionar o valor à lista, caso ainda não exista.
  
### <a name="to-create-a-form-template-that-can-add-new-items-to-a-combo-box-based-on-a-sharepoint-list"></a>Para criar um modelo de formulário que possa adicionar novos itens a uma caixa de combinação com base em uma lista do SharePoint

1. Crie uma lista personalizada simples em um servidor do SharePoint Server 2010 e nomee-a como MyList. O exemplo a seguir usa **uma caixa de combinação** vinculada ao campo **Título** dessa lista. 
    
2. Crie um novo **Formulário em** Branco no InfoPath Designer, insira um controle **Caixa** de Combinação em seu formulário e renomeie o campo vinculado à caixa de combinação como myCombo.
    
3. Crie a conexão de dados com a lista que será usada para preencher a caixa de combinação usando as seguintes etapas:
    
    1. Na guia **Dados,** clique **no botão Da Lista do SharePoint** no grupo Obter Dados **Externos.** 
        
    2. Insira a URL do site que contém a lista e clique em **Próximo.**
        
    3. Selecione a lista e clique em **Próximo.**
        
    4. Selecione os campos que você deseja incluir, para este exemplo, selecione Título e ID. O título contém os valores para a busca. Clique em **Avançar**.
        
    5. Clique **em Next** na tela a seguir. 
        
    6. Nome da conexão de dados LookupList e clique em **Concluir.**
    
4. Preencha os valores na caixa de combinação da lista usando as seguintes etapas:
    
    1. Selecione a caixa de combinação que você criou na etapa 1.
        
    2. Clique **em Editar Opções** na guia Propriedades das Ferramentas **de** Controle da faixa de opções. 
        
    3. Selecione **Obter opções de uma fonte de dados externa.**
        
    4. Certifique-se **de que a** fonte de dados está definida como a conexão de dados criada na etapa 2. 
        
    5. De definir o valor e o nome de exibição como Título.
        
    6. Na guia **Formulários do navegador,** selecione **Sempre** em Configurações de **Postback** e clique em **OK** para fechar a caixa de diálogo de propriedades. 
    
5. Certifique-se de que a caixa de combinação ainda esteja selecionada e clique em **Evento** Alterado na guia **Desenvolvedor** da faixa de opções. 
    
    Se o formulário ainda não estiver salvo, você será solicitado a salvá-lo. Em seguida, a janela do editor de código é aberta com o cursor no manipulador  `myCombo_Changed` de eventos. 
    
6. Adicione uma referência ao assembly Microsoft.SharePoint.dll como descrito anteriormente neste tópico. Para obter mais informações sobre como fazer referência ao assembly Microsoft.SharePoint, consulte [Usar membros do modelo de objeto do SharePoint.](how-to-use-sharepoint-object-model-members.md)
    
7. Colar o código a seguir no manipulador  `myCombo_Changed` de eventos. 
    
   ```cs
    // Use InfoPath OM's ServerInfo.SharePointSiteUrl property to programmatically
    // specify the site where the form is published.
    using (SPSite FormSite = new SPSite(ServerInfo.SharePointSiteUrl.ToString()))
    {
        using (SPWeb FormWeb = FormSite.OpenWeb())
        {
            // Get the SharePoint list.
            SPList LookupList = FormWeb.Lists["MyList"];
            // Query for the item.
            SPQuery MyQuery = new SPQuery();
            // "Title" is the field (column) to search in the SharePoint list.
            // /my:myFields/my:myCombo is the xpath to the field bound to the Combo Box in the form.
            MyQuery.Query = "<Where><Eq><FieldRef Name='Title' /><Value Type='Text'>" + 
                GetDomValue("/my:myFields/my:myCombo") + "</Value></Eq></Where>";
            SPListItemCollection ReturnedItems = LookupList.GetItems(MyQuery);
            // Add the item to the SharePoint list if no items were returned in the query.
            if (ReturnedItems.Count == 0)
            {
                SPListItem NewItem = LookupList.Items.Add();
                // Set the value of the Title field in the list to the value in Combo Box on the form.
                NewItem["Title"] = GetDomValue("/my:myFields/my:myCombo");
                // Set AllowUnsafeUpdates to 'true' to temporarily allow updates to the database.
                FormWeb.AllowUnsafeUpdates = true;
                NewItem.Update();
                // Set AllowUnsafeUpdates back to 'false' to prevent further updates to the database.
                FormWeb.AllowUnsafeUpdates = false;
            }
        }
    }
   ```

   ```vb
    ' Use InfoPath OM's ServerInfo.SharePointSiteUrl property to specify the site where the form is published.
    Using FormSite As New SPSite(ServerInfo.SharePointSiteUrl.ToString())
        Using FormWeb As SPWeb = FormSite.OpenWeb()
            ' Get the SharePoint list.
            Dim LookupList As SPList = FormWeb.Lists("MyList")
            ' Query for the item.
            Dim MyQuery As New SPQuery()
            ' "Title" is the field (column) to search in the SharePoint list.
            ' my:myFields/my:myCombo is the xpath to the field bound to the Combo Box in the form.
            MyQuery.Query = "<Where><Eq><FieldRef Name='Title' /><Value Type='Text'>" &amp; _
                GetDomValue("/my:myFields/my:myCombo") &amp; "</Value></Eq></Where>"
            Dim ReturnedItems As SPListItemCollection = LookupList.GetItems(MyQuery)
            ' Add the item to the lookup list if no items were returned in the query.
            If ReturnedItems.Count = 0 Then
                Dim NewItem As SPListItem = LookupList.Items.Add()
                ' Set the value of the Title field in the list to the value in Combo Box on the form.
                NewItem("Title") = GetDomValue("/my:myFields/my:myCombo")
                ' Set AllowUnsafeUpdates to 'true' to temporarily allow updates to the database.
                FormWeb.AllowUnsafeUpdates = True
                NewItem.Update()
                ' Set AllowUnsafeUpdates back to 'false' to prevent further updates to the database.
                FormWeb.AllowUnsafeUpdates = False
            End If
        End Using
    End Using
   ```

8. O exemplo de código anterior depende da  `GetDomValue` função auxiliar. Paste the following code for the  `GetDomValue` helper function below the  `myCombo_Changed` event handler function. 
    
   ```cs
    private string GetDomValue(string XpathToGet)
    {
        return this.CreateNavigator().SelectSingleNode(XpathToGet, this.NamespaceManager).Value;
    }
   ```

   ```vb
    Private Function GetDomValue(XpathToGet As String) As String
        Return Me.CreateNavigator().SelectSingleNode(XpathToGet, Me.NamespaceManager).Value
    End Function
   ```

9. Publique seu formulário usando as seguintes etapas:
    
    1. Clique **em SharePoint Server** na guia **Publicar** no Backstage. 
        
    2. Insira a URL do site do SharePoint para publicar e clique em **Próximo.** 
        
       > [!IMPORTANT]
       > Você deve ser um administrador de conjunto de sites neste site para publicar esse modelo de formulário como uma solução em áreas de segurança. 
    
    3. Selecione **a Biblioteca de** Formulário e clique em **Próximo.**
        
    4. Selecione **Criar uma nova biblioteca de formulário** e clique em **Próximo.**
        
    5. Insira o nome e a descrição da biblioteca de formulário e clique em **Próximo.**
        
    6. Clique em **Publicar**.
        
    7. Depois que o formulário for publicado com êxito, abra-o na biblioteca de formulário e adicione um novo valor à caixa de combinação para testar o código. Quando você sair do campo myCombo, o novo valor será gravado na lista do SharePoint. 
    

