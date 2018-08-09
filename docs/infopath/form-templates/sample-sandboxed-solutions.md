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
# <a name="sample-sandboxed-solutions"></a><span data-ttu-id="d00b0-103">Exemplos de soluções em área restrita</span><span class="sxs-lookup"><span data-stu-id="d00b0-103">Sample sandboxed solutions</span></span>

<span data-ttu-id="d00b0-104">Os formulários do InfoPath com código gerenciado podem ser publicados para a infraestrutura de solução em área restrita do SharePoint do InfoPath Designer.</span><span class="sxs-lookup"><span data-stu-id="d00b0-104">InfoPath forms with managed code can be published to the SharePoint sandboxed solution infrastructure from the InfoPath Designer.</span></span> <span data-ttu-id="d00b0-105">Este tópico fornece dois exemplos que mostram o tipo de código que você pode escrever em uma solução em área restrita do InfoPath e como publicar o modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="d00b0-105">This topic provides two examples that show the kind of code that you can write in an InfoPath sandboxed solution, and how to publish the form template.</span></span>
  
## <a name="example-1-sorting-data-in-an-order-form"></a><span data-ttu-id="d00b0-106">O exemplo 1: Classificar dados em um formulário de pedido</span><span class="sxs-lookup"><span data-stu-id="d00b0-106">Example 1: Sorting data in an order form</span></span>

<span data-ttu-id="d00b0-107">Classificar dados em uma tabela de repetição é uma tarefa útil que você pode executar usando o código em um formulário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d00b0-107">A useful task that you can perform by using code in an InfoPath form is to sort data in a repeating table.</span></span> <span data-ttu-id="d00b0-108">Para fazer isso, o código reordena os nós no documento XML subjacente que é exibido no formulário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d00b0-108">To do this, the code reorders the nodes in underlying XML document that is displayed in the InfoPath form.</span></span> <span data-ttu-id="d00b0-109">Embora o cenário descrito neste tópico destina-se a publicação diretamente do InfoPath como uma solução em área restrita, ele também pode ser implantado como um modelo de formulário aprovados pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="d00b0-109">Although the scenario described in this topic is targeted for publishing directly from InfoPath as a sandboxed solution, it can also be deployed as an administrator-approved form template.</span></span>
  
<span data-ttu-id="d00b0-110">Antes de começar, certifique-se de que você atende aos seguintes requisitos.</span><span class="sxs-lookup"><span data-stu-id="d00b0-110">Before you start, make sure that you meet the following requirements.</span></span>
  
- <span data-ttu-id="d00b0-111">Você é um administrador de conjunto de sites no site do SharePoint Server 2010 ou o SharePoint Foundation 2010 onde você deseja publicar o formulário.</span><span class="sxs-lookup"><span data-stu-id="d00b0-111">You are a site collection administrator on the SharePoint Server 2010 or SharePoint Foundation 2010 site where you want to publish the form.</span></span>
    
- <span data-ttu-id="d00b0-112">Verifique com o administrador do farm para certificar-se de que o serviço de código em modo seguro do Microsoft SharePoint Foundation está em execução no servidor.</span><span class="sxs-lookup"><span data-stu-id="d00b0-112">Check with the farm administrator to make sure that the Microsoft SharePoint Foundation Sandboxed Code Service is running on the server.</span></span> <span data-ttu-id="d00b0-113">Para obter mais informações, consulte [Publicando formulários com código](publishing-forms-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="d00b0-113">For more information, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span>
    
- <span data-ttu-id="d00b0-114">A linguagem de programação que você selecionou para o modelo de formulário é **c#** ou **Visual Basic** sem qualquer nome de versão anterior depois dela.</span><span class="sxs-lookup"><span data-stu-id="d00b0-114">The programming language that you have selected for the form template is either **C#** or **Visual Basic** without any earlier version name after it.</span></span> <span data-ttu-id="d00b0-115">Não há suporte para as versões compatíveis com o InfoPath 2007 e InfoPath 2003 compatíveis dos modelos de objeto e linguagens de programação para soluções em área restrita.</span><span class="sxs-lookup"><span data-stu-id="d00b0-115">The InfoPath 2007-compatible and InfoPath 2003-compatible versions of the programming languages and object models are not supported for sandboxed solutions.</span></span> <span data-ttu-id="d00b0-116">Para obter mais informações sobre como especificar a linguagem de programação, consulte [Develop com o Visual Studio](how-to-develop-with-visual-studio.md).</span><span class="sxs-lookup"><span data-stu-id="d00b0-116">For more information about how to specify the programming language, see [Develop with Visual Studio](how-to-develop-with-visual-studio.md).</span></span>
    
<span data-ttu-id="d00b0-117">Execute as seguintes etapas para criar um modelo de formulário que classifica os dados em um controle de **Tabela de repetição** no formulário.</span><span class="sxs-lookup"><span data-stu-id="d00b0-117">Perform the following steps to create a form template that sorts the data in a **Repeating Table** control on the form.</span></span> 
  
### <a name="to-create-a-form-template-that-programmatically-sorts-data-in-the-form"></a><span data-ttu-id="d00b0-118">Para criar um modelo de formulário que programaticamente classifica os dados do formulário</span><span class="sxs-lookup"><span data-stu-id="d00b0-118">To create a form template that programmatically sorts data in the form</span></span>

1. <span data-ttu-id="d00b0-119">Criar um novo modelo de formulário no InfoPath designer e adicionar um controle de **Tabela de repetição** ao formulário.</span><span class="sxs-lookup"><span data-stu-id="d00b0-119">Create a new form template in the InfoPath designer, and add a **Repeating Table** control to the form.</span></span> <span data-ttu-id="d00b0-120">O código de amostra para que esse exemplo classifica as linhas com base na primeira coluna da tabela, mas você pode modificar facilmente o código para trabalhar com qualquer coluna.</span><span class="sxs-lookup"><span data-stu-id="d00b0-120">The sample code for this example sorts the rows based on the first column in the table, but you can easily modify the code to work with any column.</span></span> 
    
2. <span data-ttu-id="d00b0-121">Adicione um controle de **botão** ao formulário.</span><span class="sxs-lookup"><span data-stu-id="d00b0-121">Add a **Button** control to the form.</span></span> <span data-ttu-id="d00b0-122">O código para classificar a tabela será adicionado ao manipulador de eventos para o evento do botão **Clicked** , mas você também pode usar outro evento para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="d00b0-122">The code to sort the table will be added to the event handler for the button's **Clicked** event, but you could also use another event for this purpose.</span></span> 
    
3. <span data-ttu-id="d00b0-123">Selecione o botão, clique na guia **Propriedades** e clique em **Código personalizado**.</span><span class="sxs-lookup"><span data-stu-id="d00b0-123">Select the button, click the **Properties** tab, and then click **Custom Code**.</span></span> <span data-ttu-id="d00b0-124">Se o seu formulário ainda não foi salvo ainda, você será solicitado a salvar a ele e, em seguida, o Editor de código será aberto com o cursor no manipulador de eventos do botão.</span><span class="sxs-lookup"><span data-stu-id="d00b0-124">If your form hasn't been saved yet, you are prompted to save it, and then the Code Editor will open with the cursor in the button's event handler.</span></span>
    
4. <span data-ttu-id="d00b0-125">Cole o seguinte código no manipulador de eventos do botão.</span><span class="sxs-lookup"><span data-stu-id="d00b0-125">Paste the following code into the button's event handler.</span></span> <span data-ttu-id="d00b0-126">O código coloca os elementos da primeira coluna em uma matriz, classifica a matriz e, em seguida, reordena a tabela com base em matriz classificada.</span><span class="sxs-lookup"><span data-stu-id="d00b0-126">The code puts the elements from the first column into an array, sorts the array, and then reorders the table based on the sorted array.</span></span> <span data-ttu-id="d00b0-127">Este código supõe que os dados sendo classificados dados de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d00b0-127">This code assumes that the data being sorted is string data.</span></span>
    
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

5. <span data-ttu-id="d00b0-128">Publica seu formulário usando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d00b0-128">Publish your form by using the following steps:</span></span>
    
    1. <span data-ttu-id="d00b0-129">Clique em **SharePoint Server** , na guia **Publicar** no Backstage.</span><span class="sxs-lookup"><span data-stu-id="d00b0-129">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="d00b0-130">Insira a URL do site do SharePoint para publicar e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d00b0-130">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="d00b0-131">Você deve ser um administrador de conjunto de sites neste site para publicar esse modelo de formulário como uma solução em área restrita.</span><span class="sxs-lookup"><span data-stu-id="d00b0-131">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="d00b0-132">Selecione a **Biblioteca de formulários**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d00b0-132">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="d00b0-133">Selecione **criar uma nova biblioteca de formulários**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d00b0-133">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="d00b0-134">Insira o nome e as descrições para sua biblioteca de formulários e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d00b0-134">Enter the name and descriptions for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="d00b0-135">Clique em **Publicar**.</span><span class="sxs-lookup"><span data-stu-id="d00b0-135">Click **Publish**.</span></span>
    
## <a name="example-2-managing-vendors-in-a-sharepoint-list"></a><span data-ttu-id="d00b0-136">Exemplo 2: Gerenciando fornecedores em uma lista do SharePoint</span><span class="sxs-lookup"><span data-stu-id="d00b0-136">Example 2: Managing vendors in a SharePoint list</span></span>

<span data-ttu-id="d00b0-137">Este exemplo envolve programação em relação ao modelo de objeto do Microsoft SharePoint Foundation 2010.</span><span class="sxs-lookup"><span data-stu-id="d00b0-137">This example involves programming against the Microsoft SharePoint Foundation 2010 object model.</span></span> <span data-ttu-id="d00b0-138">Para fazer isso, você precisa estabelecer uma referência para o assembly Microsoft.SharePoint.dll que é instalado com uma cópia licenciada do SharePoint Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d00b0-138">To do that, you must establish a reference to the Microsoft.SharePoint.dll assembly which is installed with a licensed copy of SharePoint Server 2010.</span></span>
  
<span data-ttu-id="d00b0-139">Microsoft.SharePoint.Server.dll é instalado em C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI por padrão.</span><span class="sxs-lookup"><span data-stu-id="d00b0-139">Microsoft.SharePoint.Server.dll is installed in C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI by default.</span></span> <span data-ttu-id="d00b0-140">Esta DLL deve ser incluído nos projetos em que o modelo de objeto programe o SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d00b0-140">This DLL must be included in projects where you program against the SharePoint object model.</span></span> <span data-ttu-id="d00b0-141">Para estabelecer uma referência para a Microsoft.SharePoint.dll em um projeto do Visual Studio 2012, abra o **Editor de código**e, em seguida, no menu **Ferramentas** , clique em **Adicionar referência** .</span><span class="sxs-lookup"><span data-stu-id="d00b0-141">To establish a reference to the Microsoft.SharePoint.dll in a Visual Studio 2012 project, open the **Code Editor**, and then click **Add Reference** on the **Tools** menu.</span></span> <span data-ttu-id="d00b0-142">Na caixa de diálogo **Adicionar referência** , clique na guia **Procurar** , especifique o local do arquivo Microsoft.SharePoint.dll e, em seguida, clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="d00b0-142">In the **Add Reference** dialog box, click the **Browse** tab, specify the location of the Microsoft.SharePoint.dll file, and then click **OK**.</span></span> <span data-ttu-id="d00b0-143">Isso irá copiar a Microsoft.SharePoint.dll no diretório do projeto para que você possa usar membros de modelo de objeto do SharePoint Foundation 2010 em sua solução do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d00b0-143">This will copy the Microsoft.SharePoint.dll into the project directory so that you can use SharePoint Foundation 2010 object model members in your InfoPath solution.</span></span>
  
### <a name="designing-the-form-and-developing-the-code"></a><span data-ttu-id="d00b0-144">Projetando o formulário e o código de desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="d00b0-144">Designing the form and developing the code</span></span>

<span data-ttu-id="d00b0-145">A partir de código em um formulário do InfoPath, você pode usar o modelo de objeto do SharePoint para criar itens nas listas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d00b0-145">From code in an InfoPath form, you can use the SharePoint object model to create items in lookup lists.</span></span> <span data-ttu-id="d00b0-146">Isso é útil quando você preencher uma caixa de lista suspensa de uma lista do SharePoint e deseja adicionar novos valores a ele sem criar um formulário separado.</span><span class="sxs-lookup"><span data-stu-id="d00b0-146">This is useful when you populate a drop-down box from a SharePoint list and want to add new values to it without creating a separate form.</span></span> <span data-ttu-id="d00b0-147">Este exemplo usa uma caixa de combinação para mostrar todos os valores atualmente na lista e cria a lógica de programação para adicionar o valor à lista, se ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="d00b0-147">This example uses a combo box to show all the values currently in the list and creates programming logic to add the value to the list if it does not already exist.</span></span>
  
### <a name="to-create-a-form-template-that-can-add-new-items-to-a-combo-box-based-on-a-sharepoint-list"></a><span data-ttu-id="d00b0-148">Para criar um modelo de formulário que pode adicionar novos itens a uma caixa de combinação com base em uma lista do SharePoint</span><span class="sxs-lookup"><span data-stu-id="d00b0-148">To create a form template that can add new items to a combo box based on a SharePoint list</span></span>

1. <span data-ttu-id="d00b0-149">Criar uma lista personalizada simple em um servidor do SharePoint Server 2010 e nomeie-o MyList.</span><span class="sxs-lookup"><span data-stu-id="d00b0-149">Create a simple custom list on a SharePoint Server 2010 server, and name it MyList.</span></span> <span data-ttu-id="d00b0-150">O exemplo a seguir usa uma **Caixa de combinação** acoplada a campo **título** desta lista.</span><span class="sxs-lookup"><span data-stu-id="d00b0-150">The following example uses a **Combo Box** bound to the **Title** field of this list.</span></span> 
    
2. <span data-ttu-id="d00b0-151">Criar um novo **Formulário em branco** no InfoPath Designer, inserir um controle de **Caixa de combinação** em seu formulário e renomear o campo vinculado à caixa de combinação para myCombo.</span><span class="sxs-lookup"><span data-stu-id="d00b0-151">Create a new **Blank Form** in InfoPath Designer, insert a **Combo Box** control on your form, and rename the field bound to the combo box to myCombo.</span></span>
    
3. <span data-ttu-id="d00b0-152">Crie a conexão de dados para a lista que será usada para preencher a caixa de combinação usando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d00b0-152">Create the data connection to the list that will be used to populate the combo box by using the following steps:</span></span>
    
    1. <span data-ttu-id="d00b0-153">Na guia **dados** , clique no botão **De lista do SharePoint** no grupo **Obter dados externos** .</span><span class="sxs-lookup"><span data-stu-id="d00b0-153">On the **Data** tab, click **From SharePoint List** button in the **Get External Data** group.</span></span> 
        
    2. <span data-ttu-id="d00b0-154">Digite a URL para o site que contém a lista e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d00b0-154">Enter the URL for the site that contains the list, and then click **Next**.</span></span>
        
    3. <span data-ttu-id="d00b0-155">Selecione a lista e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d00b0-155">Select the list, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="d00b0-156">Selecione os campos que você deseja incluir, neste exemplo, selecione o título e a ID.</span><span class="sxs-lookup"><span data-stu-id="d00b0-156">Select the fields that you want to include, for this example, select Title and ID.</span></span> <span data-ttu-id="d00b0-157">Título contém os valores de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d00b0-157">Title contains the values for lookup.</span></span> <span data-ttu-id="d00b0-158">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d00b0-158">Click **Next**.</span></span>
        
    5. <span data-ttu-id="d00b0-159">Clique em **Avançar** na tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d00b0-159">Click **Next** on the following screen.</span></span> 
        
    6. <span data-ttu-id="d00b0-160">Nomeie a conexão de dados LookupList e clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="d00b0-160">Name the data connection LookupList, and then click **Finish**.</span></span>
    
4. <span data-ttu-id="d00b0-161">Preencha os valores na caixa de combinação da lista, usando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d00b0-161">Populate the values in the combo box from the list by using the following steps:</span></span>
    
    1. <span data-ttu-id="d00b0-162">Marque a caixa de combinação que você criou na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="d00b0-162">Select the combo box that you created in step 1.</span></span>
        
    2. <span data-ttu-id="d00b0-163">Clique em **Editar escolhas** na guia **Propriedades de ferramentas de controle** da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="d00b0-163">Click **Edit Choices** on the **Control Tools Properties** tab of the ribbon.</span></span> 
        
    3. <span data-ttu-id="d00b0-164">Selecione **fazer as escolhas de uma fonte de dados externos**.</span><span class="sxs-lookup"><span data-stu-id="d00b0-164">Select **Get choices from an external data source**.</span></span>
        
    4. <span data-ttu-id="d00b0-165">Certifique-se de que a **fonte de dados** está definido como a conexão de dados que você criou na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="d00b0-165">Make sure that **Data source** is set to the data connection that you created in step 2.</span></span> 
        
    5. <span data-ttu-id="d00b0-166">Definir o valor e o nome de exibição para o título.</span><span class="sxs-lookup"><span data-stu-id="d00b0-166">Set the value and display name to Title.</span></span>
        
    6. <span data-ttu-id="d00b0-167">Na guia **formulários de navegador** , selecione **sempre** em **Postback configurações**e, em seguida, clique em **Okey** para fechar a caixa de diálogo de propriedades.</span><span class="sxs-lookup"><span data-stu-id="d00b0-167">On the **Browser forms** tab, select **Always** under **Postback settings**, and then click **OK** to close the properties dialog box.</span></span> 
    
5. <span data-ttu-id="d00b0-168">Certificar-se de que a caixa de combinação ainda está marcada e clique em **Evento alterado** na guia **desenvolvedor** da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="d00b0-168">Make sure the combo box is still selected, and then click **Changed Event** on the **Developer** tab of the ribbon.</span></span> 
    
    <span data-ttu-id="d00b0-169">Se o seu formulário ainda não foi salva, você precisará salvá-lo.</span><span class="sxs-lookup"><span data-stu-id="d00b0-169">If your form is not saved yet, you are prompted to save it.</span></span> <span data-ttu-id="d00b0-170">E, em seguida, a janela do editor de código abre com o cursor no `myCombo_Changed` manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="d00b0-170">And then, the code editor window opens with the cursor in the  `myCombo_Changed` event handler.</span></span> 
    
6. <span data-ttu-id="d00b0-171">Adicione uma referência para o assembly Microsoft.SharePoint.dll conforme descrito anteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="d00b0-171">Add a reference to the Microsoft.SharePoint.dll assembly as described earlier in this topic.</span></span> <span data-ttu-id="d00b0-172">Para obter mais informações sobre como fazer referência a assembly do Microsoft, consulte [Use membros do modelo de objeto do SharePoint](how-to-use-sharepoint-object-model-members.md).</span><span class="sxs-lookup"><span data-stu-id="d00b0-172">For more information about referencing the Microsoft.SharePoint assembly, see [Use SharePoint Object Model Members](how-to-use-sharepoint-object-model-members.md).</span></span>
    
7. <span data-ttu-id="d00b0-173">Cole o seguinte código no `myCombo_Changed` manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="d00b0-173">Paste the following code into the  `myCombo_Changed` event handler.</span></span> 
    
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

8. <span data-ttu-id="d00b0-174">O exemplo de código anterior depende do `GetDomValue` função auxiliar.</span><span class="sxs-lookup"><span data-stu-id="d00b0-174">The preceding code example depends on the  `GetDomValue` helper function.</span></span> <span data-ttu-id="d00b0-175">Cole o seguinte código para o `GetDomValue` função auxiliar abaixo do `myCombo_Changed` função do manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="d00b0-175">Paste the following code for the  `GetDomValue` helper function below the  `myCombo_Changed` event handler function.</span></span> 
    
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

9. <span data-ttu-id="d00b0-176">Publica seu formulário usando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d00b0-176">Publish your form by using the following steps:</span></span>
    
    1. <span data-ttu-id="d00b0-177">Clique em **SharePoint Server** , na guia **Publicar** no Backstage.</span><span class="sxs-lookup"><span data-stu-id="d00b0-177">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="d00b0-178">Insira a URL do site do SharePoint para publicar e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d00b0-178">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="d00b0-179">Você deve ser um administrador de conjunto de sites neste site para publicar esse modelo de formulário como uma solução em área restrita.</span><span class="sxs-lookup"><span data-stu-id="d00b0-179">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="d00b0-180">Selecione a **Biblioteca de formulários**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d00b0-180">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="d00b0-181">Selecione **criar uma nova biblioteca de formulários**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d00b0-181">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="d00b0-182">Insira o nome e descrição para a sua biblioteca de formulários e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d00b0-182">Enter the name and description for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="d00b0-183">Clique em **Publicar**.</span><span class="sxs-lookup"><span data-stu-id="d00b0-183">Click **Publish**.</span></span>
        
    7. <span data-ttu-id="d00b0-184">Depois que o formulário seja publicado com êxito, abra o formulário da biblioteca de formulários e adicione um novo valor na caixa de combinação para testar o código.</span><span class="sxs-lookup"><span data-stu-id="d00b0-184">After the form is successfully published, open the form from the form library and add a new value into the combo box to test the code.</span></span> <span data-ttu-id="d00b0-185">Quando você sai do campo de myCombo, o novo valor será gravado na lista do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d00b0-185">When you exit the myCombo field, the new value will be written to the SharePoint list.</span></span> 
    

