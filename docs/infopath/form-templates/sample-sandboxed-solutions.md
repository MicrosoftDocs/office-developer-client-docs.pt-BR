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
# <a name="sample-sandboxed-solutions"></a><span data-ttu-id="5d49e-103">Exemplo de soluções em modo seguro</span><span class="sxs-lookup"><span data-stu-id="5d49e-103">Sample sandboxed solutions</span></span>

<span data-ttu-id="5d49e-104">Os formulários do InfoPath com código gerenciado podem ser publicados na infraestrutura de solução em área restrita do SharePoint a partir do InfoPath designer.</span><span class="sxs-lookup"><span data-stu-id="5d49e-104">InfoPath forms with managed code can be published to the SharePoint sandboxed solution infrastructure from the InfoPath Designer.</span></span> <span data-ttu-id="5d49e-105">Este tópico fornece dois exemplos que mostram o tipo de código que você pode escrever em uma solução de área restrita do InfoPath e como publicar o modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="5d49e-105">This topic provides two examples that show the kind of code that you can write in an InfoPath sandboxed solution, and how to publish the form template.</span></span>
  
## <a name="example-1-sorting-data-in-an-order-form"></a><span data-ttu-id="5d49e-106">Exemplo 1: classificar dados em um formulário de pedido</span><span class="sxs-lookup"><span data-stu-id="5d49e-106">Example 1: Sorting data in an order form</span></span>

<span data-ttu-id="5d49e-107">Uma tarefa útil que você pode executar usando o código em um formulário do InfoPath é classificar dados em uma tabela de repetição.</span><span class="sxs-lookup"><span data-stu-id="5d49e-107">A useful task that you can perform by using code in an InfoPath form is to sort data in a repeating table.</span></span> <span data-ttu-id="5d49e-108">Para fazer isso, o código reordena os nós no documento XML subjacente que é exibido no formulário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="5d49e-108">To do this, the code reorders the nodes in underlying XML document that is displayed in the InfoPath form.</span></span> <span data-ttu-id="5d49e-109">Embora o cenário descrito neste tópico seja direcionado para publicação diretamente do InfoPath como uma solução de área restrita, ele também pode ser implantado como um modelo de formulário aprovado pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="5d49e-109">Although the scenario described in this topic is targeted for publishing directly from InfoPath as a sandboxed solution, it can also be deployed as an administrator-approved form template.</span></span>
  
<span data-ttu-id="5d49e-110">Antes de começar, verifique se você atende aos seguintes requisitos.</span><span class="sxs-lookup"><span data-stu-id="5d49e-110">Before you start, make sure that you meet the following requirements.</span></span>
  
- <span data-ttu-id="5d49e-111">Você é um administrador do conjunto de sites no site do SharePoint Server 2010 ou SharePoint Foundation 2010 onde você deseja publicar o formulário.</span><span class="sxs-lookup"><span data-stu-id="5d49e-111">You are a site collection administrator on the SharePoint Server 2010 or SharePoint Foundation 2010 site where you want to publish the form.</span></span>
    
- <span data-ttu-id="5d49e-112">Consulte o administrador do farm para verificar se o serviço de código em área restrita do Microsoft SharePoint Foundation está em execução no servidor.</span><span class="sxs-lookup"><span data-stu-id="5d49e-112">Check with the farm administrator to make sure that the Microsoft SharePoint Foundation Sandboxed Code Service is running on the server.</span></span> <span data-ttu-id="5d49e-113">Para mais informações, consulte [publicAndo formulários com código](publishing-forms-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="5d49e-113">For more information, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span>
    
- <span data-ttu-id="5d49e-114">A linguagem de programação que você selecionou para o modelo de formulário é **C#** ou **Visual Basic** sem qualquer nome de versão anterior.</span><span class="sxs-lookup"><span data-stu-id="5d49e-114">The programming language that you have selected for the form template is either **C#** or **Visual Basic** without any earlier version name after it.</span></span> <span data-ttu-id="5d49e-115">As versões compatíveis com o InfoPath 2007 e o InfoPath 2003 compatíveis com as linguagens de programação e modelos de objeto não têm suporte para soluções de área restrita.</span><span class="sxs-lookup"><span data-stu-id="5d49e-115">The InfoPath 2007-compatible and InfoPath 2003-compatible versions of the programming languages and object models are not supported for sandboxed solutions.</span></span> <span data-ttu-id="5d49e-116">Para obter mais informações sobre como especificar a linguagem de programação, consulte [desenvolvimento com o Visual Studio](how-to-develop-with-visual-studio.md).</span><span class="sxs-lookup"><span data-stu-id="5d49e-116">For more information about how to specify the programming language, see [Develop with Visual Studio](how-to-develop-with-visual-studio.md).</span></span>
    
<span data-ttu-id="5d49e-117">Execute as etapas a seguir para criar um modelo de formulário que classifique os dados em um controle de **tabela de repetição** no formulário.</span><span class="sxs-lookup"><span data-stu-id="5d49e-117">Perform the following steps to create a form template that sorts the data in a **Repeating Table** control on the form.</span></span> 
  
### <a name="to-create-a-form-template-that-programmatically-sorts-data-in-the-form"></a><span data-ttu-id="5d49e-118">Para criar um modelo de formulário que classifica dados de forma programática no formulário</span><span class="sxs-lookup"><span data-stu-id="5d49e-118">To create a form template that programmatically sorts data in the form</span></span>

1. <span data-ttu-id="5d49e-119">Crie um novo modelo de formulário no designer do InfoPath e adicione um controle de **tabela de repetição** ao formulário.</span><span class="sxs-lookup"><span data-stu-id="5d49e-119">Create a new form template in the InfoPath designer, and add a **Repeating Table** control to the form.</span></span> <span data-ttu-id="5d49e-120">O código de exemplo deste exemplo classifica as linhas com base na primeira coluna da tabela, mas você pode facilmente modificar o código para trabalhar com qualquer coluna.</span><span class="sxs-lookup"><span data-stu-id="5d49e-120">The sample code for this example sorts the rows based on the first column in the table, but you can easily modify the code to work with any column.</span></span> 
    
2. <span data-ttu-id="5d49e-121">Adicionar um controle de **botão** ao formulário.</span><span class="sxs-lookup"><span data-stu-id="5d49e-121">Add a **Button** control to the form.</span></span> <span data-ttu-id="5d49e-122">O código para classificar a tabela será adicionado ao manipulador de eventos para o evento clicado \*\*\*\* do botão, mas você também pode usar outro evento para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="5d49e-122">The code to sort the table will be added to the event handler for the button's **Clicked** event, but you could also use another event for this purpose.</span></span> 
    
3. <span data-ttu-id="5d49e-123">Selecione o botão, clique na guia **Propriedades** e, em seguida, clique em **código personalizado**.</span><span class="sxs-lookup"><span data-stu-id="5d49e-123">Select the button, click the **Properties** tab, and then click **Custom Code**.</span></span> <span data-ttu-id="5d49e-124">Se o formulário ainda não tiver sido salvo, você será solicitado a salvá-lo e, em seguida, o editor de código será aberto com o cursor no manipulador de eventos do botão.</span><span class="sxs-lookup"><span data-stu-id="5d49e-124">If your form hasn't been saved yet, you are prompted to save it, and then the Code Editor will open with the cursor in the button's event handler.</span></span>
    
4. <span data-ttu-id="5d49e-125">Cole o seguinte código no manipulador de eventos do botão.</span><span class="sxs-lookup"><span data-stu-id="5d49e-125">Paste the following code into the button's event handler.</span></span> <span data-ttu-id="5d49e-126">O código coloca os elementos da primeira coluna em uma matriz, classifica a matriz e, em seguida, reordena a tabela com base na matriz classificada.</span><span class="sxs-lookup"><span data-stu-id="5d49e-126">The code puts the elements from the first column into an array, sorts the array, and then reorders the table based on the sorted array.</span></span> <span data-ttu-id="5d49e-127">Esse código pressupõe que os dados que estão sendo classificados são dados de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5d49e-127">This code assumes that the data being sorted is string data.</span></span>
    
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

5. <span data-ttu-id="5d49e-128">Publique seu formulário usando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="5d49e-128">Publish your form by using the following steps:</span></span>
    
    1. <span data-ttu-id="5d49e-129">Clique em **SharePoint Server** na guia **publicar** no backstage.</span><span class="sxs-lookup"><span data-stu-id="5d49e-129">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="5d49e-130">Insira a URL do site do SharePoint para publicar e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5d49e-130">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="5d49e-131">Você deve ser um administrador de conjunto de sites neste site para publicar este modelo de formulário como uma solução de área restrita.</span><span class="sxs-lookup"><span data-stu-id="5d49e-131">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="5d49e-132">Selecione **biblioteca de formulários**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5d49e-132">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="5d49e-133">Selecione **criar uma nova biblioteca de formulários**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5d49e-133">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="5d49e-134">Insira o nome e as descrições da sua biblioteca de formulários e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5d49e-134">Enter the name and descriptions for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="5d49e-135">Clique em **publicar**.</span><span class="sxs-lookup"><span data-stu-id="5d49e-135">Click **Publish**.</span></span>
    
## <a name="example-2-managing-vendors-in-a-sharepoint-list"></a><span data-ttu-id="5d49e-136">Exemplo 2: Gerenciando fornecedores em uma lista do SharePoint</span><span class="sxs-lookup"><span data-stu-id="5d49e-136">Example 2: Managing vendors in a SharePoint list</span></span>

<span data-ttu-id="5d49e-137">Este exemplo envolve a programação em relação ao modelo de objeto do Microsoft SharePoint Foundation 2010.</span><span class="sxs-lookup"><span data-stu-id="5d49e-137">This example involves programming against the Microsoft SharePoint Foundation 2010 object model.</span></span> <span data-ttu-id="5d49e-138">Para fazer isso, você deve estabelecer uma referência ao assembly Microsoft. SharePoint. dll que é instalado com uma cópia licenciada do SharePoint Server 2010.</span><span class="sxs-lookup"><span data-stu-id="5d49e-138">To do that, you must establish a reference to the Microsoft.SharePoint.dll assembly which is installed with a licensed copy of SharePoint Server 2010.</span></span>
  
<span data-ttu-id="5d49e-139">Microsoft. SharePoint. Server. dll está instalado em C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI por padrão.</span><span class="sxs-lookup"><span data-stu-id="5d49e-139">Microsoft.SharePoint.Server.dll is installed in C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI by default.</span></span> <span data-ttu-id="5d49e-140">Essa DLL deve estar incluída nos projetos em que você programar contra o modelo de objeto do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5d49e-140">This DLL must be included in projects where you program against the SharePoint object model.</span></span> <span data-ttu-id="5d49e-141">Para estabelecer uma referência para o Microsoft. SharePoint. dll em um projeto do Visual Studio 2012, abra o **Editor de código**e, em seguida, clique em **Adicionar referência** no menu **ferramentas** .</span><span class="sxs-lookup"><span data-stu-id="5d49e-141">To establish a reference to the Microsoft.SharePoint.dll in a Visual Studio 2012 project, open the **Code Editor**, and then click **Add Reference** on the **Tools** menu.</span></span> <span data-ttu-id="5d49e-142">Na caixa de diálogo **Adicionar referência** , clique na guia **procurar** , especifique o local do arquivo Microsoft. SharePoint. dll e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d49e-142">In the **Add Reference** dialog box, click the **Browse** tab, specify the location of the Microsoft.SharePoint.dll file, and then click **OK**.</span></span> <span data-ttu-id="5d49e-143">Isso copiará o Microsoft. SharePoint. dll no diretório do projeto para que você possa usar membros do modelo de objeto do SharePoint Foundation 2010 em sua solução do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="5d49e-143">This will copy the Microsoft.SharePoint.dll into the project directory so that you can use SharePoint Foundation 2010 object model members in your InfoPath solution.</span></span>
  
### <a name="designing-the-form-and-developing-the-code"></a><span data-ttu-id="5d49e-144">Criando o formulário e desenvolvendo o código</span><span class="sxs-lookup"><span data-stu-id="5d49e-144">Designing the form and developing the code</span></span>

<span data-ttu-id="5d49e-145">A partir do código em um formulário do InfoPath, você pode usar o modelo de objeto do SharePoint para criar itens em listas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5d49e-145">From code in an InfoPath form, you can use the SharePoint object model to create items in lookup lists.</span></span> <span data-ttu-id="5d49e-146">Isso é útil quando você preenche uma caixa suspensa de uma lista do SharePoint e deseja adicionar novos valores a ela sem criar um formulário separado.</span><span class="sxs-lookup"><span data-stu-id="5d49e-146">This is useful when you populate a drop-down box from a SharePoint list and want to add new values to it without creating a separate form.</span></span> <span data-ttu-id="5d49e-147">Este exemplo usa uma caixa de combinação para mostrar todos os valores atualmente na lista e cria uma lógica de programação para adicionar o valor à lista, caso ainda não exista.</span><span class="sxs-lookup"><span data-stu-id="5d49e-147">This example uses a combo box to show all the values currently in the list and creates programming logic to add the value to the list if it does not already exist.</span></span>
  
### <a name="to-create-a-form-template-that-can-add-new-items-to-a-combo-box-based-on-a-sharepoint-list"></a><span data-ttu-id="5d49e-148">Para criar um modelo de formulário que possa adicionar novos itens a uma caixa de combinação com base em uma lista do SharePoint</span><span class="sxs-lookup"><span data-stu-id="5d49e-148">To create a form template that can add new items to a combo box based on a SharePoint list</span></span>

1. <span data-ttu-id="5d49e-149">Crie uma lista personalizada simples em um servidor do SharePoint Server 2010 e nomeie-a como myList.</span><span class="sxs-lookup"><span data-stu-id="5d49e-149">Create a simple custom list on a SharePoint Server 2010 server, and name it MyList.</span></span> <span data-ttu-id="5d49e-150">O exemplo a seguir usa uma **caixa de combinação** acoplada ao campo de **título** desta lista.</span><span class="sxs-lookup"><span data-stu-id="5d49e-150">The following example uses a **Combo Box** bound to the **Title** field of this list.</span></span> 
    
2. <span data-ttu-id="5d49e-151">Criar um novo **formulário em branco** no designer do InfoPath, inserir um controle de **caixa de combinação** no formulário e renomear o campo associado à caixa de combinação para mycombo.</span><span class="sxs-lookup"><span data-stu-id="5d49e-151">Create a new **Blank Form** in InfoPath Designer, insert a **Combo Box** control on your form, and rename the field bound to the combo box to myCombo.</span></span>
    
3. <span data-ttu-id="5d49e-152">Crie a conexão de dados com a lista que será usada para preencher a caixa de combinação usando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="5d49e-152">Create the data connection to the list that will be used to populate the combo box by using the following steps:</span></span>
    
    1. <span data-ttu-id="5d49e-153">Na guia **dados** , clique no botão **de lista do SharePoint** no grupo **obter dados externos** .</span><span class="sxs-lookup"><span data-stu-id="5d49e-153">On the **Data** tab, click **From SharePoint List** button in the **Get External Data** group.</span></span> 
        
    2. <span data-ttu-id="5d49e-154">Insira a URL do site que contém a lista e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5d49e-154">Enter the URL for the site that contains the list, and then click **Next**.</span></span>
        
    3. <span data-ttu-id="5d49e-155">Selecione a lista e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5d49e-155">Select the list, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="5d49e-156">Selecione os campos que você deseja incluir para este exemplo, selecione título e ID.</span><span class="sxs-lookup"><span data-stu-id="5d49e-156">Select the fields that you want to include, for this example, select Title and ID.</span></span> <span data-ttu-id="5d49e-157">Título contém os valores para pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5d49e-157">Title contains the values for lookup.</span></span> <span data-ttu-id="5d49e-158">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5d49e-158">Click **Next**.</span></span>
        
    5. <span data-ttu-id="5d49e-159">Clique em **Avançar** na tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5d49e-159">Click **Next** on the following screen.</span></span> 
        
    6. <span data-ttu-id="5d49e-160">Nomeie a pesquisa de conexão de dados e clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="5d49e-160">Name the data connection LookupList, and then click **Finish**.</span></span>
    
4. <span data-ttu-id="5d49e-161">Preencha os valores na caixa de combinação da lista usando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="5d49e-161">Populate the values in the combo box from the list by using the following steps:</span></span>
    
    1. <span data-ttu-id="5d49e-162">Selecione a caixa de combinação que você criou na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="5d49e-162">Select the combo box that you created in step 1.</span></span>
        
    2. <span data-ttu-id="5d49e-163">Clique em **Editar opções** na guia **Propriedades de ferramentas de controle** da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="5d49e-163">Click **Edit Choices** on the **Control Tools Properties** tab of the ribbon.</span></span> 
        
    3. <span data-ttu-id="5d49e-164">Selecione **obter opções de uma fonte de dados externa**.</span><span class="sxs-lookup"><span data-stu-id="5d49e-164">Select **Get choices from an external data source**.</span></span>
        
    4. <span data-ttu-id="5d49e-165">Certifique-se de que a **fonte de dados** está definida como a conexão de dados que você criou na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="5d49e-165">Make sure that **Data source** is set to the data connection that you created in step 2.</span></span> 
        
    5. <span data-ttu-id="5d49e-166">Definir o valor e o nome para exibição como título.</span><span class="sxs-lookup"><span data-stu-id="5d49e-166">Set the value and display name to Title.</span></span>
        
    6. <span data-ttu-id="5d49e-167">Na guia **formulários do navegador** , selecione **sempre** em **configurações de postback**e, em seguida, clique em **OK** para fechar a caixa de diálogo Propriedades.</span><span class="sxs-lookup"><span data-stu-id="5d49e-167">On the **Browser forms** tab, select **Always** under **Postback settings**, and then click **OK** to close the properties dialog box.</span></span> 
    
5. <span data-ttu-id="5d49e-168">Certifique-se de que a caixa de combinação ainda esteja selecionada e, em seguida, clique em **alterar evento** na guia **desenvolvedor** da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="5d49e-168">Make sure the combo box is still selected, and then click **Changed Event** on the **Developer** tab of the ribbon.</span></span> 
    
    <span data-ttu-id="5d49e-169">Se o formulário ainda não tiver sido salvo, você será solicitado a salvá-lo.</span><span class="sxs-lookup"><span data-stu-id="5d49e-169">If your form is not saved yet, you are prompted to save it.</span></span> <span data-ttu-id="5d49e-170">E, em seguida, a janela do editor de código abre com `myCombo_Changed` o cursor no manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="5d49e-170">And then, the code editor window opens with the cursor in the  `myCombo_Changed` event handler.</span></span> 
    
6. <span data-ttu-id="5d49e-171">Adicione uma referência ao assembly Microsoft. SharePoint. dll conforme descrito anteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="5d49e-171">Add a reference to the Microsoft.SharePoint.dll assembly as described earlier in this topic.</span></span> <span data-ttu-id="5d49e-172">Para obter mais informações sobre como fazer referência ao assembly Microsoft. SharePoint, consulte [usar membros do modelo de objeto do SharePoint](how-to-use-sharepoint-object-model-members.md).</span><span class="sxs-lookup"><span data-stu-id="5d49e-172">For more information about referencing the Microsoft.SharePoint assembly, see [Use SharePoint Object Model Members](how-to-use-sharepoint-object-model-members.md).</span></span>
    
7. <span data-ttu-id="5d49e-173">Cole o seguinte código no manipulador `myCombo_Changed` de eventos.</span><span class="sxs-lookup"><span data-stu-id="5d49e-173">Paste the following code into the  `myCombo_Changed` event handler.</span></span> 
    
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

8. <span data-ttu-id="5d49e-174">O exemplo de código anterior depende da `GetDomValue` função auxiliar.</span><span class="sxs-lookup"><span data-stu-id="5d49e-174">The preceding code example depends on the  `GetDomValue` helper function.</span></span> <span data-ttu-id="5d49e-175">Cole o código a seguir para `GetDomValue` a função auxiliar abaixo `myCombo_Changed` da função do manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="5d49e-175">Paste the following code for the  `GetDomValue` helper function below the  `myCombo_Changed` event handler function.</span></span> 
    
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

9. <span data-ttu-id="5d49e-176">Publique seu formulário usando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="5d49e-176">Publish your form by using the following steps:</span></span>
    
    1. <span data-ttu-id="5d49e-177">Clique em **SharePoint Server** na guia **publicar** no backstage.</span><span class="sxs-lookup"><span data-stu-id="5d49e-177">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="5d49e-178">Insira a URL do site do SharePoint para publicar e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5d49e-178">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="5d49e-179">Você deve ser um administrador de conjunto de sites neste site para publicar este modelo de formulário como uma solução de área restrita.</span><span class="sxs-lookup"><span data-stu-id="5d49e-179">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="5d49e-180">Selecione **biblioteca de formulários**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5d49e-180">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="5d49e-181">Selecione **criar uma nova biblioteca de formulários**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5d49e-181">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="5d49e-182">Insira o nome e a descrição da sua biblioteca de formulários e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5d49e-182">Enter the name and description for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="5d49e-183">Clique em **publicar**.</span><span class="sxs-lookup"><span data-stu-id="5d49e-183">Click **Publish**.</span></span>
        
    7. <span data-ttu-id="5d49e-184">Depois que o formulário for publicado com êxito, abra o formulário na biblioteca de formulários e adicione um novo valor à caixa de combinação para testar o código.</span><span class="sxs-lookup"><span data-stu-id="5d49e-184">After the form is successfully published, open the form from the form library and add a new value into the combo box to test the code.</span></span> <span data-ttu-id="5d49e-185">Quando você sair do campo myCombo, o novo valor será gravado na lista do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5d49e-185">When you exit the myCombo field, the new value will be written to the SharePoint list.</span></span> 
    

