---
title: Exemplo de soluções em modo seguro
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 415fa0fa-b7b7-4acb-a437-f54c34064004
description: Este tópico fornece dois exemplos que mostram o tipo de código que você pode escrever em uma solução de área restrita do InfoPath e como publicar o modelo de formulário.
ms.openlocfilehash: 56a9a2a765100ef327790265c7cf734903268bed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439335"
---
# <a name="sample-sandboxed-solutions"></a>Exemplo de soluções em modo seguro

Os formulários do InfoPath com código gerenciado podem ser publicados na infraestrutura de solução em área restrita do SharePoint a partir do InfoPath designer. Este tópico fornece dois exemplos que mostram o tipo de código que você pode escrever em uma solução de área restrita do InfoPath e como publicar o modelo de formulário.
  
## <a name="example-1-sorting-data-in-an-order-form"></a>Exemplo 1: classificar dados em um formulário de pedido

Uma tarefa útil que você pode executar usando o código em um formulário do InfoPath é classificar dados em uma tabela de repetição. Para fazer isso, o código reordena os nós no documento XML subjacente que é exibido no formulário do InfoPath. Embora o cenário descrito neste tópico seja direcionado para publicação diretamente do InfoPath como uma solução de área restrita, ele também pode ser implantado como um modelo de formulário aprovado pelo administrador.
  
Antes de começar, verifique se você atende aos seguintes requisitos.
  
- Você é um administrador do conjunto de sites no site do SharePoint Server 2010 ou SharePoint Foundation 2010 onde você deseja publicar o formulário.
    
- Consulte o administrador do farm para verificar se o serviço de código em área restrita do Microsoft SharePoint Foundation está em execução no servidor. Para mais informações, consulte [publicAndo formulários com código](publishing-forms-with-code.md).
    
- A linguagem de programação que você selecionou para o modelo de formulário é **C#** ou **Visual Basic** sem qualquer nome de versão anterior. As versões compatíveis com o InfoPath 2007 e o InfoPath 2003 compatíveis com as linguagens de programação e modelos de objeto não têm suporte para soluções de área restrita. Para obter mais informações sobre como especificar a linguagem de programação, consulte [desenvolvimento com o Visual Studio](how-to-develop-with-visual-studio.md).
    
Execute as etapas a seguir para criar um modelo de formulário que classifique os dados em um controle de **tabela de repetição** no formulário. 
  
### <a name="to-create-a-form-template-that-programmatically-sorts-data-in-the-form"></a>Para criar um modelo de formulário que classifica dados de forma programática no formulário

1. Crie um novo modelo de formulário no designer do InfoPath e adicione um controle de **tabela de repetição** ao formulário. O código de exemplo deste exemplo classifica as linhas com base na primeira coluna da tabela, mas você pode facilmente modificar o código para trabalhar com qualquer coluna. 
    
2. Adicionar um controle de **botão** ao formulário. O código para classificar a tabela será adicionado ao manipulador de eventos para o evento clicado **** do botão, mas você também pode usar outro evento para essa finalidade. 
    
3. Selecione o botão, clique na guia **Propriedades** e, em seguida, clique em **código personalizado**. Se o formulário ainda não tiver sido salvo, você será solicitado a salvá-lo e, em seguida, o editor de código será aberto com o cursor no manipulador de eventos do botão.
    
4. Cole o seguinte código no manipulador de eventos do botão. O código coloca os elementos da primeira coluna em uma matriz, classifica a matriz e, em seguida, reordena a tabela com base na matriz classificada. Esse código pressupõe que os dados que estão sendo classificados são dados de cadeia de caracteres.
    
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
    
    1. Clique em **SharePoint Server** na guia **publicar** no backstage. 
        
    2. Insira a URL do site do SharePoint para publicar e clique em **Avançar**. 
        
       > [!IMPORTANT]
       > Você deve ser um administrador de conjunto de sites neste site para publicar este modelo de formulário como uma solução de área restrita. 
    
    3. Selecione **biblioteca de formulários**e clique em **Avançar**.
        
    4. Selecione **criar uma nova biblioteca de formulários**e clique em **Avançar**.
        
    5. Insira o nome e as descrições da sua biblioteca de formulários e clique em **Avançar**.
        
    6. Clique em **publicar**.
    
## <a name="example-2-managing-vendors-in-a-sharepoint-list"></a>Exemplo 2: Gerenciando fornecedores em uma lista do SharePoint

Este exemplo envolve a programação em relação ao modelo de objeto do Microsoft SharePoint Foundation 2010. Para fazer isso, você deve estabelecer uma referência ao assembly Microsoft. SharePoint. dll que é instalado com uma cópia licenciada do SharePoint Server 2010.
  
Microsoft. SharePoint. Server. dll está instalado em C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI por padrão. Essa DLL deve estar incluída nos projetos em que você programar contra o modelo de objeto do SharePoint. Para estabelecer uma referência para o Microsoft. SharePoint. dll em um projeto do Visual Studio 2012, abra o **Editor de código**e, em seguida, clique em **Adicionar referência** no menu **ferramentas** . Na caixa de diálogo **Adicionar referência** , clique na guia **procurar** , especifique o local do arquivo Microsoft. SharePoint. dll e, em seguida, clique em **OK**. Isso copiará o Microsoft. SharePoint. dll no diretório do projeto para que você possa usar membros do modelo de objeto do SharePoint Foundation 2010 em sua solução do InfoPath.
  
### <a name="designing-the-form-and-developing-the-code"></a>Criando o formulário e desenvolvendo o código

A partir do código em um formulário do InfoPath, você pode usar o modelo de objeto do SharePoint para criar itens em listas de pesquisa. Isso é útil quando você preenche uma caixa suspensa de uma lista do SharePoint e deseja adicionar novos valores a ela sem criar um formulário separado. Este exemplo usa uma caixa de combinação para mostrar todos os valores atualmente na lista e cria uma lógica de programação para adicionar o valor à lista, caso ainda não exista.
  
### <a name="to-create-a-form-template-that-can-add-new-items-to-a-combo-box-based-on-a-sharepoint-list"></a>Para criar um modelo de formulário que possa adicionar novos itens a uma caixa de combinação com base em uma lista do SharePoint

1. Crie uma lista personalizada simples em um servidor do SharePoint Server 2010 e nomeie-a como myList. O exemplo a seguir usa uma **caixa de combinação** acoplada ao campo de **título** desta lista. 
    
2. Criar um novo **formulário em branco** no designer do InfoPath, inserir um controle de **caixa de combinação** no formulário e renomear o campo associado à caixa de combinação para mycombo.
    
3. Crie a conexão de dados com a lista que será usada para preencher a caixa de combinação usando as seguintes etapas:
    
    1. Na guia **dados** , clique no botão **de lista do SharePoint** no grupo **obter dados externos** . 
        
    2. Insira a URL do site que contém a lista e clique em **Avançar**.
        
    3. Selecione a lista e clique em **Avançar**.
        
    4. Selecione os campos que você deseja incluir para este exemplo, selecione título e ID. Título contém os valores para pesquisa. Clique em **Avançar**.
        
    5. Clique em **Avançar** na tela a seguir. 
        
    6. Nomeie a pesquisa de conexão de dados e clique em **concluir**.
    
4. Preencha os valores na caixa de combinação da lista usando as seguintes etapas:
    
    1. Selecione a caixa de combinação que você criou na etapa 1.
        
    2. Clique em **Editar opções** na guia **Propriedades de ferramentas de controle** da faixa de opções. 
        
    3. Selecione **obter opções de uma fonte de dados externa**.
        
    4. Certifique-se de que a **fonte de dados** está definida como a conexão de dados que você criou na etapa 2. 
        
    5. Definir o valor e o nome para exibição como título.
        
    6. Na guia **formulários do navegador** , selecione **sempre** em **configurações de postback**e, em seguida, clique em **OK** para fechar a caixa de diálogo Propriedades. 
    
5. Certifique-se de que a caixa de combinação ainda esteja selecionada e, em seguida, clique em **alterar evento** na guia **desenvolvedor** da faixa de opções. 
    
    Se o formulário ainda não tiver sido salvo, você será solicitado a salvá-lo. E, em seguida, a janela do editor de código abre com `myCombo_Changed` o cursor no manipulador de eventos. 
    
6. Adicione uma referência ao assembly Microsoft. SharePoint. dll conforme descrito anteriormente neste tópico. Para obter mais informações sobre como fazer referência ao assembly Microsoft. SharePoint, consulte [usar membros do modelo de objeto do SharePoint](how-to-use-sharepoint-object-model-members.md).
    
7. Cole o seguinte código no manipulador `myCombo_Changed` de eventos. 
    
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

8. O exemplo de código anterior depende da `GetDomValue` função auxiliar. Cole o código a seguir para `GetDomValue` a função auxiliar abaixo `myCombo_Changed` da função do manipulador de eventos. 
    
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
    
    1. Clique em **SharePoint Server** na guia **publicar** no backstage. 
        
    2. Insira a URL do site do SharePoint para publicar e clique em **Avançar**. 
        
       > [!IMPORTANT]
       > Você deve ser um administrador de conjunto de sites neste site para publicar este modelo de formulário como uma solução de área restrita. 
    
    3. Selecione **biblioteca de formulários**e clique em **Avançar**.
        
    4. Selecione **criar uma nova biblioteca de formulários**e clique em **Avançar**.
        
    5. Insira o nome e a descrição da sua biblioteca de formulários e clique em **Avançar**.
        
    6. Clique em **publicar**.
        
    7. Depois que o formulário for publicado com êxito, abra o formulário na biblioteca de formulários e adicione um novo valor à caixa de combinação para testar o código. Quando você sair do campo myCombo, o novo valor será gravado na lista do SharePoint. 
    

