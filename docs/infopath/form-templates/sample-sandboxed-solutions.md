---
title: Exemplos de soluções em área restrita
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 415fa0fa-b7b7-4acb-a437-f54c34064004
description: Este tópico fornece dois exemplos que mostram o tipo de código que você pode escrever em uma solução em área restrita do InfoPath e como publicar o modelo de formulário.
ms.openlocfilehash: b0874e34d843850df55eee87d689ce0d01112635
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765706"
---
# <a name="sample-sandboxed-solutions"></a>Exemplos de soluções em área restrita

Os formulários do InfoPath com código gerenciado podem ser publicados para a infraestrutura de solução em área restrita do SharePoint do InfoPath Designer. Este tópico fornece dois exemplos que mostram o tipo de código que você pode escrever em uma solução em área restrita do InfoPath e como publicar o modelo de formulário.
  
## <a name="example-1-sorting-data-in-an-order-form"></a>O exemplo 1: Classificar dados em um formulário de pedido

Classificar dados em uma tabela de repetição é uma tarefa útil que você pode executar usando o código em um formulário do InfoPath. Para fazer isso, o código reordena os nós no documento XML subjacente que é exibido no formulário do InfoPath. Embora o cenário descrito neste tópico destina-se a publicação diretamente do InfoPath como uma solução em área restrita, ele também pode ser implantado como um modelo de formulário aprovados pelo administrador.
  
Antes de começar, certifique-se de que você atende aos seguintes requisitos.
  
- Você é um administrador de conjunto de sites no site do SharePoint Server 2010 ou o SharePoint Foundation 2010 onde você deseja publicar o formulário.
    
- Verifique com o administrador do farm para certificar-se de que o serviço de código em modo seguro do Microsoft SharePoint Foundation está em execução no servidor. Para obter mais informações, consulte [Publicando formulários com código](publishing-forms-with-code.md).
    
- A linguagem de programação que você selecionou para o modelo de formulário é **c#** ou **Visual Basic** sem qualquer nome de versão anterior depois dela. Não há suporte para as versões compatíveis com o InfoPath 2007 e InfoPath 2003 compatíveis dos modelos de objeto e linguagens de programação para soluções em área restrita. Para obter mais informações sobre como especificar a linguagem de programação, consulte [Develop com o Visual Studio](how-to-develop-with-visual-studio.md).
    
Execute as seguintes etapas para criar um modelo de formulário que classifica os dados em um controle de **Tabela de repetição** no formulário. 
  
### <a name="to-create-a-form-template-that-programmatically-sorts-data-in-the-form"></a>Para criar um modelo de formulário que programaticamente classifica os dados do formulário

1. Criar um novo modelo de formulário no InfoPath designer e adicionar um controle de **Tabela de repetição** ao formulário. O código de amostra para que esse exemplo classifica as linhas com base na primeira coluna da tabela, mas você pode modificar facilmente o código para trabalhar com qualquer coluna. 
    
2. Adicione um controle de **botão** ao formulário. O código para classificar a tabela será adicionado ao manipulador de eventos para o evento do botão **Clicked** , mas você também pode usar outro evento para essa finalidade. 
    
3. Selecione o botão, clique na guia **Propriedades** e clique em **Código personalizado**. Se o seu formulário ainda não foi salvo ainda, você será solicitado a salvar a ele e, em seguida, o Editor de código será aberto com o cursor no manipulador de eventos do botão.
    
4. Cole o seguinte código no manipulador de eventos do botão. O código coloca os elementos da primeira coluna em uma matriz, classifica a matriz e, em seguida, reordena a tabela com base em matriz classificada. Este código supõe que os dados sendo classificados dados de cadeia de caracteres.
    
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

5. Publica seu formulário usando as seguintes etapas:
    
    1. Clique em **SharePoint Server** , na guia **Publicar** no Backstage. 
        
    2. Insira a URL do site do SharePoint para publicar e, em seguida, clique em **Avançar**. 
        
       > [!IMPORTANT]
       > Você deve ser um administrador de conjunto de sites neste site para publicar esse modelo de formulário como uma solução em área restrita. 
    
    3. Selecione a **Biblioteca de formulários**e clique em **Avançar**.
        
    4. Selecione **criar uma nova biblioteca de formulários**e clique em **Avançar**.
        
    5. Insira o nome e as descrições para sua biblioteca de formulários e clique em **Avançar**.
        
    6. Clique em **Publicar**.
    
## <a name="example-2-managing-vendors-in-a-sharepoint-list"></a>Exemplo 2: Gerenciando fornecedores em uma lista do SharePoint

Este exemplo envolve programação em relação ao modelo de objeto do Microsoft SharePoint Foundation 2010. Para fazer isso, você precisa estabelecer uma referência para o assembly Microsoft.SharePoint.dll que é instalado com uma cópia licenciada do SharePoint Server 2010.
  
Microsoft.SharePoint.Server.dll é instalado em C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI por padrão. Esta DLL deve ser incluído nos projetos em que o modelo de objeto programe o SharePoint. Para estabelecer uma referência para a Microsoft.SharePoint.dll em um projeto do Visual Studio 2012, abra o **Editor de código**e, em seguida, no menu **Ferramentas** , clique em **Adicionar referência** . Na caixa de diálogo **Adicionar referência** , clique na guia **Procurar** , especifique o local do arquivo Microsoft.SharePoint.dll e, em seguida, clique em **Okey**. Isso irá copiar a Microsoft.SharePoint.dll no diretório do projeto para que você possa usar membros de modelo de objeto do SharePoint Foundation 2010 em sua solução do InfoPath.
  
### <a name="designing-the-form-and-developing-the-code"></a>Projetando o formulário e o código de desenvolvimento

A partir de código em um formulário do InfoPath, você pode usar o modelo de objeto do SharePoint para criar itens nas listas de pesquisa. Isso é útil quando você preencher uma caixa de lista suspensa de uma lista do SharePoint e deseja adicionar novos valores a ele sem criar um formulário separado. Este exemplo usa uma caixa de combinação para mostrar todos os valores atualmente na lista e cria a lógica de programação para adicionar o valor à lista, se ainda não existir.
  
### <a name="to-create-a-form-template-that-can-add-new-items-to-a-combo-box-based-on-a-sharepoint-list"></a>Para criar um modelo de formulário que pode adicionar novos itens a uma caixa de combinação com base em uma lista do SharePoint

1. Criar uma lista personalizada simple em um servidor do SharePoint Server 2010 e nomeie-o MyList. O exemplo a seguir usa uma **Caixa de combinação** acoplada a campo **título** desta lista. 
    
2. Criar um novo **Formulário em branco** no InfoPath Designer, inserir um controle de **Caixa de combinação** em seu formulário e renomear o campo vinculado à caixa de combinação para myCombo.
    
3. Crie a conexão de dados para a lista que será usada para preencher a caixa de combinação usando as seguintes etapas:
    
    1. Na guia **dados** , clique no botão **De lista do SharePoint** no grupo **Obter dados externos** . 
        
    2. Digite a URL para o site que contém a lista e clique em **Avançar**.
        
    3. Selecione a lista e clique em **Avançar**.
        
    4. Selecione os campos que você deseja incluir, neste exemplo, selecione o título e a ID. Título contém os valores de pesquisa. Clique em **Avançar**.
        
    5. Clique em **Avançar** na tela a seguir. 
        
    6. Nomeie a conexão de dados LookupList e clique em **Concluir**.
    
4. Preencha os valores na caixa de combinação da lista, usando as seguintes etapas:
    
    1. Marque a caixa de combinação que você criou na etapa 1.
        
    2. Clique em **Editar escolhas** na guia **Propriedades de ferramentas de controle** da faixa de opções. 
        
    3. Selecione **fazer as escolhas de uma fonte de dados externos**.
        
    4. Certifique-se de que a **fonte de dados** está definido como a conexão de dados que você criou na etapa 2. 
        
    5. Definir o valor e o nome de exibição para o título.
        
    6. Na guia **formulários de navegador** , selecione **sempre** em **Postback configurações**e, em seguida, clique em **Okey** para fechar a caixa de diálogo de propriedades. 
    
5. Certificar-se de que a caixa de combinação ainda está marcada e clique em **Evento alterado** na guia **desenvolvedor** da faixa de opções. 
    
    Se o seu formulário ainda não foi salva, você precisará salvá-lo. E, em seguida, a janela do editor de código abre com o cursor no `myCombo_Changed` manipulador de eventos. 
    
6. Adicione uma referência para o assembly Microsoft.SharePoint.dll conforme descrito anteriormente neste tópico. Para obter mais informações sobre como fazer referência a assembly do Microsoft, consulte [Use membros do modelo de objeto do SharePoint](how-to-use-sharepoint-object-model-members.md).
    
7. Cole o seguinte código no `myCombo_Changed` manipulador de eventos. 
    
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

8. O exemplo de código anterior depende do `GetDomValue` função auxiliar. Cole o seguinte código para o `GetDomValue` função auxiliar abaixo do `myCombo_Changed` função do manipulador de eventos. 
    
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

9. Publica seu formulário usando as seguintes etapas:
    
    1. Clique em **SharePoint Server** , na guia **Publicar** no Backstage. 
        
    2. Insira a URL do site do SharePoint para publicar e, em seguida, clique em **Avançar**. 
        
       > [!IMPORTANT]
       > Você deve ser um administrador de conjunto de sites neste site para publicar esse modelo de formulário como uma solução em área restrita. 
    
    3. Selecione a **Biblioteca de formulários**e clique em **Avançar**.
        
    4. Selecione **criar uma nova biblioteca de formulários**e clique em **Avançar**.
        
    5. Insira o nome e descrição para a sua biblioteca de formulários e clique em **Avançar**.
        
    6. Clique em **Publicar**.
        
    7. Depois que o formulário seja publicado com êxito, abra o formulário da biblioteca de formulários e adicione um novo valor na caixa de combinação para testar o código. Quando você sai do campo de myCombo, o novo valor será gravado na lista do SharePoint. 
    

