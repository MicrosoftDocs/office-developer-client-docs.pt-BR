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
# <a name="sample-sandboxed-solutions"></a><span data-ttu-id="359e7-103">Exemplo de soluções em modo seguro</span><span class="sxs-lookup"><span data-stu-id="359e7-103">Sample sandboxed solutions</span></span>

<span data-ttu-id="359e7-104">Os formulários do InfoPath com código gerenciado podem ser publicados na infraestrutura de soluções em áreas alternativas do SharePoint do InfoPath Designer.</span><span class="sxs-lookup"><span data-stu-id="359e7-104">InfoPath forms with managed code can be published to the SharePoint sandboxed solution infrastructure from the InfoPath Designer.</span></span> <span data-ttu-id="359e7-105">Este tópico fornece dois exemplos que mostram o tipo de código que você pode escrever em uma solução em áreas de segurança do InfoPath e como publicar o modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="359e7-105">This topic provides two examples that show the kind of code that you can write in an InfoPath sandboxed solution, and how to publish the form template.</span></span>
  
## <a name="example-1-sorting-data-in-an-order-form"></a><span data-ttu-id="359e7-106">Exemplo 1: Classificar dados em um formulário de pedido</span><span class="sxs-lookup"><span data-stu-id="359e7-106">Example 1: Sorting data in an order form</span></span>

<span data-ttu-id="359e7-107">Uma tarefa útil que você pode executar usando código em um formulário do InfoPath é classificar dados em uma tabela de repetição.</span><span class="sxs-lookup"><span data-stu-id="359e7-107">A useful task that you can perform by using code in an InfoPath form is to sort data in a repeating table.</span></span> <span data-ttu-id="359e7-108">Para fazer isso, o código reordena os nós no documento XML subjacente que é exibido no formulário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="359e7-108">To do this, the code reorders the nodes in underlying XML document that is displayed in the InfoPath form.</span></span> <span data-ttu-id="359e7-109">Embora o cenário descrito neste tópico seja direcionado para publicação diretamente do InfoPath como uma solução em áreas de segurança, ele também pode ser implantado como um modelo de formulário aprovado pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="359e7-109">Although the scenario described in this topic is targeted for publishing directly from InfoPath as a sandboxed solution, it can also be deployed as an administrator-approved form template.</span></span>
  
<span data-ttu-id="359e7-110">Antes de começar, certifique-se de que você está de acordo com os requisitos a seguir.</span><span class="sxs-lookup"><span data-stu-id="359e7-110">Before you start, make sure that you meet the following requirements.</span></span>
  
- <span data-ttu-id="359e7-111">Você é um administrador de conjunto de sites no site do SharePoint Server 2010 ou do SharePoint Foundation 2010 em que deseja publicar o formulário.</span><span class="sxs-lookup"><span data-stu-id="359e7-111">You are a site collection administrator on the SharePoint Server 2010 or SharePoint Foundation 2010 site where you want to publish the form.</span></span>
    
- <span data-ttu-id="359e7-112">Verifique com o administrador do farm se o Serviço de Código em Área Segura do Microsoft SharePoint Foundation está em execução no servidor.</span><span class="sxs-lookup"><span data-stu-id="359e7-112">Check with the farm administrator to make sure that the Microsoft SharePoint Foundation Sandboxed Code Service is running on the server.</span></span> <span data-ttu-id="359e7-113">Para obter mais informações, [consulte Formulários de Publicação com Código.](publishing-forms-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="359e7-113">For more information, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span>
    
- <span data-ttu-id="359e7-114">A linguagem de programação que você selecionou para o modelo de formulário é **C#** ou **Visual Basic** sem qualquer nome de versão anterior depois dela.</span><span class="sxs-lookup"><span data-stu-id="359e7-114">The programming language that you have selected for the form template is either **C#** or **Visual Basic** without any earlier version name after it.</span></span> <span data-ttu-id="359e7-115">As versões compatíveis com o InfoPath 2007 e compatíveis com o InfoPath 2003 das linguagens de programação e modelos de objeto não têm suporte para soluções em áreas alternativas.</span><span class="sxs-lookup"><span data-stu-id="359e7-115">The InfoPath 2007-compatible and InfoPath 2003-compatible versions of the programming languages and object models are not supported for sandboxed solutions.</span></span> <span data-ttu-id="359e7-116">Para obter mais informações sobre como especificar a linguagem de programação, consulte [Desenvolver com o Visual Studio.](how-to-develop-with-visual-studio.md)</span><span class="sxs-lookup"><span data-stu-id="359e7-116">For more information about how to specify the programming language, see [Develop with Visual Studio](how-to-develop-with-visual-studio.md).</span></span>
    
<span data-ttu-id="359e7-117">Execute as etapas a seguir para criar um modelo de formulário que classifica os dados em um **controle tabela** de repetição no formulário.</span><span class="sxs-lookup"><span data-stu-id="359e7-117">Perform the following steps to create a form template that sorts the data in a **Repeating Table** control on the form.</span></span> 
  
### <a name="to-create-a-form-template-that-programmatically-sorts-data-in-the-form"></a><span data-ttu-id="359e7-118">Para criar um modelo de formulário que classifica programaticamente os dados no formulário</span><span class="sxs-lookup"><span data-stu-id="359e7-118">To create a form template that programmatically sorts data in the form</span></span>

1. <span data-ttu-id="359e7-119">Crie um novo modelo de formulário no designer do InfoPath e adicione um **controle De tabela** de repetição ao formulário.</span><span class="sxs-lookup"><span data-stu-id="359e7-119">Create a new form template in the InfoPath designer, and add a **Repeating Table** control to the form.</span></span> <span data-ttu-id="359e7-120">O código de exemplo para este exemplo classifica as linhas com base na primeira coluna da tabela, mas você pode modificar facilmente o código para trabalhar com qualquer coluna.</span><span class="sxs-lookup"><span data-stu-id="359e7-120">The sample code for this example sorts the rows based on the first column in the table, but you can easily modify the code to work with any column.</span></span> 
    
2. <span data-ttu-id="359e7-121">Adicione um **controle Button** ao formulário.</span><span class="sxs-lookup"><span data-stu-id="359e7-121">Add a **Button** control to the form.</span></span> <span data-ttu-id="359e7-122">O código para classificar a tabela será adicionado ao manipulador de eventos para o evento **Clicked** do botão, mas você também pode usar outro evento para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="359e7-122">The code to sort the table will be added to the event handler for the button's **Clicked** event, but you could also use another event for this purpose.</span></span> 
    
3. <span data-ttu-id="359e7-123">Selecione o botão, clique na guia **Propriedades** e clique em **Código Personalizado.**</span><span class="sxs-lookup"><span data-stu-id="359e7-123">Select the button, click the **Properties** tab, and then click **Custom Code**.</span></span> <span data-ttu-id="359e7-124">Se o formulário ainda não tiver sido salvo, você será solicitado a salvá-lo e, em seguida, o Editor de Código abrirá com o cursor no manipulador de eventos do botão.</span><span class="sxs-lookup"><span data-stu-id="359e7-124">If your form hasn't been saved yet, you are prompted to save it, and then the Code Editor will open with the cursor in the button's event handler.</span></span>
    
4. <span data-ttu-id="359e7-125">Colar o código a seguir no manipulador de eventos do botão.</span><span class="sxs-lookup"><span data-stu-id="359e7-125">Paste the following code into the button's event handler.</span></span> <span data-ttu-id="359e7-126">O código coloca os elementos da primeira coluna em uma matriz, classifica a matriz e reordena a tabela com base na matriz ordenada.</span><span class="sxs-lookup"><span data-stu-id="359e7-126">The code puts the elements from the first column into an array, sorts the array, and then reorders the table based on the sorted array.</span></span> <span data-ttu-id="359e7-127">Este código assume que os dados que estão sendo organizados são dados de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="359e7-127">This code assumes that the data being sorted is string data.</span></span>
    
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

5. <span data-ttu-id="359e7-128">Publique seu formulário usando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="359e7-128">Publish your form by using the following steps:</span></span>
    
    1. <span data-ttu-id="359e7-129">Clique **em SharePoint Server** na guia **Publicar** no Backstage.</span><span class="sxs-lookup"><span data-stu-id="359e7-129">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="359e7-130">Insira a URL do site do SharePoint para publicar e clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="359e7-130">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="359e7-131">Você deve ser um administrador de conjunto de sites neste site para publicar esse modelo de formulário como uma solução em áreas de segurança.</span><span class="sxs-lookup"><span data-stu-id="359e7-131">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="359e7-132">Selecione **a Biblioteca de** Formulário e clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="359e7-132">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="359e7-133">Selecione **Criar uma nova biblioteca de formulário** e clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="359e7-133">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="359e7-134">Insira o nome e as descrições da biblioteca de formulário e clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="359e7-134">Enter the name and descriptions for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="359e7-135">Clique em **Publicar**.</span><span class="sxs-lookup"><span data-stu-id="359e7-135">Click **Publish**.</span></span>
    
## <a name="example-2-managing-vendors-in-a-sharepoint-list"></a><span data-ttu-id="359e7-136">Exemplo 2: Gerenciando fornecedores em uma lista do SharePoint</span><span class="sxs-lookup"><span data-stu-id="359e7-136">Example 2: Managing vendors in a SharePoint list</span></span>

<span data-ttu-id="359e7-137">Este exemplo envolve a programação no modelo de objeto do Microsoft SharePoint Foundation 2010.</span><span class="sxs-lookup"><span data-stu-id="359e7-137">This example involves programming against the Microsoft SharePoint Foundation 2010 object model.</span></span> <span data-ttu-id="359e7-138">Para fazer isso, você deve estabelecer uma referência ao assembly Microsoft.SharePoint.dll que é instalado com uma cópia licenciada do SharePoint Server 2010.</span><span class="sxs-lookup"><span data-stu-id="359e7-138">To do that, you must establish a reference to the Microsoft.SharePoint.dll assembly which is installed with a licensed copy of SharePoint Server 2010.</span></span>
  
<span data-ttu-id="359e7-139">Microsoft.SharePoint.Server.dll é instalado em C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI por padrão.</span><span class="sxs-lookup"><span data-stu-id="359e7-139">Microsoft.SharePoint.Server.dll is installed in C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI by default.</span></span> <span data-ttu-id="359e7-140">Essa DLL deve ser incluída em projetos nos quais você programa em relação ao modelo de objeto do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="359e7-140">This DLL must be included in projects where you program against the SharePoint object model.</span></span> <span data-ttu-id="359e7-141">Para estabelecer uma referência à Microsoft.SharePoint.dll em um projeto do Visual Studio 2012, abra o **Editor** de Código e clique em Adicionar Referência no **menu** Ferramentas. </span><span class="sxs-lookup"><span data-stu-id="359e7-141">To establish a reference to the Microsoft.SharePoint.dll in a Visual Studio 2012 project, open the **Code Editor**, and then click **Add Reference** on the **Tools** menu.</span></span> <span data-ttu-id="359e7-142">Na caixa **de diálogo** Adicionar  Referência, clique na guia Procurar, especifique o local do arquivo Microsoft.SharePoint.dll e clique em **OK.**</span><span class="sxs-lookup"><span data-stu-id="359e7-142">In the **Add Reference** dialog box, click the **Browse** tab, specify the location of the Microsoft.SharePoint.dll file, and then click **OK**.</span></span> <span data-ttu-id="359e7-143">Isso copiará o Microsoft.SharePoint.dll para o diretório do projeto para que você possa usar os membros do modelo de objeto do SharePoint Foundation 2010 em sua solução do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="359e7-143">This will copy the Microsoft.SharePoint.dll into the project directory so that you can use SharePoint Foundation 2010 object model members in your InfoPath solution.</span></span>
  
### <a name="designing-the-form-and-developing-the-code"></a><span data-ttu-id="359e7-144">Projetando o formulário e desenvolvendo o código</span><span class="sxs-lookup"><span data-stu-id="359e7-144">Designing the form and developing the code</span></span>

<span data-ttu-id="359e7-145">No código em um formulário do InfoPath, você pode usar o modelo de objeto do SharePoint para criar itens em listas de análise.</span><span class="sxs-lookup"><span data-stu-id="359e7-145">From code in an InfoPath form, you can use the SharePoint object model to create items in lookup lists.</span></span> <span data-ttu-id="359e7-146">Isso é útil quando você preenche uma caixa de lista lista de uma lista do SharePoint e deseja adicionar novos valores a ela sem criar um formulário separado.</span><span class="sxs-lookup"><span data-stu-id="359e7-146">This is useful when you populate a drop-down box from a SharePoint list and want to add new values to it without creating a separate form.</span></span> <span data-ttu-id="359e7-147">Este exemplo usa uma caixa de combinação para mostrar todos os valores atualmente na lista e cria lógica de programação para adicionar o valor à lista, caso ainda não exista.</span><span class="sxs-lookup"><span data-stu-id="359e7-147">This example uses a combo box to show all the values currently in the list and creates programming logic to add the value to the list if it does not already exist.</span></span>
  
### <a name="to-create-a-form-template-that-can-add-new-items-to-a-combo-box-based-on-a-sharepoint-list"></a><span data-ttu-id="359e7-148">Para criar um modelo de formulário que possa adicionar novos itens a uma caixa de combinação com base em uma lista do SharePoint</span><span class="sxs-lookup"><span data-stu-id="359e7-148">To create a form template that can add new items to a combo box based on a SharePoint list</span></span>

1. <span data-ttu-id="359e7-149">Crie uma lista personalizada simples em um servidor do SharePoint Server 2010 e nomee-a como MyList.</span><span class="sxs-lookup"><span data-stu-id="359e7-149">Create a simple custom list on a SharePoint Server 2010 server, and name it MyList.</span></span> <span data-ttu-id="359e7-150">O exemplo a seguir usa **uma caixa de combinação** vinculada ao campo **Título** dessa lista.</span><span class="sxs-lookup"><span data-stu-id="359e7-150">The following example uses a **Combo Box** bound to the **Title** field of this list.</span></span> 
    
2. <span data-ttu-id="359e7-151">Crie um novo **Formulário em** Branco no InfoPath Designer, insira um controle **Caixa** de Combinação em seu formulário e renomeie o campo vinculado à caixa de combinação como myCombo.</span><span class="sxs-lookup"><span data-stu-id="359e7-151">Create a new **Blank Form** in InfoPath Designer, insert a **Combo Box** control on your form, and rename the field bound to the combo box to myCombo.</span></span>
    
3. <span data-ttu-id="359e7-152">Crie a conexão de dados com a lista que será usada para preencher a caixa de combinação usando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="359e7-152">Create the data connection to the list that will be used to populate the combo box by using the following steps:</span></span>
    
    1. <span data-ttu-id="359e7-153">Na guia **Dados,** clique **no botão Da Lista do SharePoint** no grupo Obter Dados **Externos.**</span><span class="sxs-lookup"><span data-stu-id="359e7-153">On the **Data** tab, click **From SharePoint List** button in the **Get External Data** group.</span></span> 
        
    2. <span data-ttu-id="359e7-154">Insira a URL do site que contém a lista e clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="359e7-154">Enter the URL for the site that contains the list, and then click **Next**.</span></span>
        
    3. <span data-ttu-id="359e7-155">Selecione a lista e clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="359e7-155">Select the list, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="359e7-156">Selecione os campos que você deseja incluir, para este exemplo, selecione Título e ID.</span><span class="sxs-lookup"><span data-stu-id="359e7-156">Select the fields that you want to include, for this example, select Title and ID.</span></span> <span data-ttu-id="359e7-157">O título contém os valores para a busca.</span><span class="sxs-lookup"><span data-stu-id="359e7-157">Title contains the values for lookup.</span></span> <span data-ttu-id="359e7-158">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="359e7-158">Click **Next**.</span></span>
        
    5. <span data-ttu-id="359e7-159">Clique **em Next** na tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="359e7-159">Click **Next** on the following screen.</span></span> 
        
    6. <span data-ttu-id="359e7-160">Nome da conexão de dados LookupList e clique em **Concluir.**</span><span class="sxs-lookup"><span data-stu-id="359e7-160">Name the data connection LookupList, and then click **Finish**.</span></span>
    
4. <span data-ttu-id="359e7-161">Preencha os valores na caixa de combinação da lista usando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="359e7-161">Populate the values in the combo box from the list by using the following steps:</span></span>
    
    1. <span data-ttu-id="359e7-162">Selecione a caixa de combinação que você criou na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="359e7-162">Select the combo box that you created in step 1.</span></span>
        
    2. <span data-ttu-id="359e7-163">Clique **em Editar Opções** na guia Propriedades das Ferramentas **de** Controle da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="359e7-163">Click **Edit Choices** on the **Control Tools Properties** tab of the ribbon.</span></span> 
        
    3. <span data-ttu-id="359e7-164">Selecione **Obter opções de uma fonte de dados externa.**</span><span class="sxs-lookup"><span data-stu-id="359e7-164">Select **Get choices from an external data source**.</span></span>
        
    4. <span data-ttu-id="359e7-165">Certifique-se **de que a** fonte de dados está definida como a conexão de dados criada na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="359e7-165">Make sure that **Data source** is set to the data connection that you created in step 2.</span></span> 
        
    5. <span data-ttu-id="359e7-166">De definir o valor e o nome de exibição como Título.</span><span class="sxs-lookup"><span data-stu-id="359e7-166">Set the value and display name to Title.</span></span>
        
    6. <span data-ttu-id="359e7-167">Na guia **Formulários do navegador,** selecione **Sempre** em Configurações de **Postback** e clique em **OK** para fechar a caixa de diálogo de propriedades.</span><span class="sxs-lookup"><span data-stu-id="359e7-167">On the **Browser forms** tab, select **Always** under **Postback settings**, and then click **OK** to close the properties dialog box.</span></span> 
    
5. <span data-ttu-id="359e7-168">Certifique-se de que a caixa de combinação ainda esteja selecionada e clique em **Evento** Alterado na guia **Desenvolvedor** da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="359e7-168">Make sure the combo box is still selected, and then click **Changed Event** on the **Developer** tab of the ribbon.</span></span> 
    
    <span data-ttu-id="359e7-169">Se o formulário ainda não estiver salvo, você será solicitado a salvá-lo.</span><span class="sxs-lookup"><span data-stu-id="359e7-169">If your form is not saved yet, you are prompted to save it.</span></span> <span data-ttu-id="359e7-170">Em seguida, a janela do editor de código é aberta com o cursor no manipulador  `myCombo_Changed` de eventos.</span><span class="sxs-lookup"><span data-stu-id="359e7-170">And then, the code editor window opens with the cursor in the  `myCombo_Changed` event handler.</span></span> 
    
6. <span data-ttu-id="359e7-171">Adicione uma referência ao assembly Microsoft.SharePoint.dll como descrito anteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="359e7-171">Add a reference to the Microsoft.SharePoint.dll assembly as described earlier in this topic.</span></span> <span data-ttu-id="359e7-172">Para obter mais informações sobre como fazer referência ao assembly Microsoft.SharePoint, consulte [Usar membros do modelo de objeto do SharePoint.](how-to-use-sharepoint-object-model-members.md)</span><span class="sxs-lookup"><span data-stu-id="359e7-172">For more information about referencing the Microsoft.SharePoint assembly, see [Use SharePoint Object Model Members](how-to-use-sharepoint-object-model-members.md).</span></span>
    
7. <span data-ttu-id="359e7-173">Colar o código a seguir no manipulador  `myCombo_Changed` de eventos.</span><span class="sxs-lookup"><span data-stu-id="359e7-173">Paste the following code into the  `myCombo_Changed` event handler.</span></span> 
    
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

8. <span data-ttu-id="359e7-174">O exemplo de código anterior depende da  `GetDomValue` função auxiliar.</span><span class="sxs-lookup"><span data-stu-id="359e7-174">The preceding code example depends on the  `GetDomValue` helper function.</span></span> <span data-ttu-id="359e7-175">Paste the following code for the  `GetDomValue` helper function below the  `myCombo_Changed` event handler function.</span><span class="sxs-lookup"><span data-stu-id="359e7-175">Paste the following code for the  `GetDomValue` helper function below the  `myCombo_Changed` event handler function.</span></span> 
    
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

9. <span data-ttu-id="359e7-176">Publique seu formulário usando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="359e7-176">Publish your form by using the following steps:</span></span>
    
    1. <span data-ttu-id="359e7-177">Clique **em SharePoint Server** na guia **Publicar** no Backstage.</span><span class="sxs-lookup"><span data-stu-id="359e7-177">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="359e7-178">Insira a URL do site do SharePoint para publicar e clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="359e7-178">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="359e7-179">Você deve ser um administrador de conjunto de sites neste site para publicar esse modelo de formulário como uma solução em áreas de segurança.</span><span class="sxs-lookup"><span data-stu-id="359e7-179">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="359e7-180">Selecione **a Biblioteca de** Formulário e clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="359e7-180">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="359e7-181">Selecione **Criar uma nova biblioteca de formulário** e clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="359e7-181">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="359e7-182">Insira o nome e a descrição da biblioteca de formulário e clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="359e7-182">Enter the name and description for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="359e7-183">Clique em **Publicar**.</span><span class="sxs-lookup"><span data-stu-id="359e7-183">Click **Publish**.</span></span>
        
    7. <span data-ttu-id="359e7-184">Depois que o formulário for publicado com êxito, abra-o na biblioteca de formulário e adicione um novo valor à caixa de combinação para testar o código.</span><span class="sxs-lookup"><span data-stu-id="359e7-184">After the form is successfully published, open the form from the form library and add a new value into the combo box to test the code.</span></span> <span data-ttu-id="359e7-185">Quando você sair do campo myCombo, o novo valor será gravado na lista do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="359e7-185">When you exit the myCombo field, the new value will be written to the SharePoint list.</span></span> 
    

