---
title: Cenário de Publicação de Internet
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f28b14f3eaf6792a74ef0967d698d5a3914955a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708505"
---
# <a name="internet-publishing-scenario"></a><span data-ttu-id="4e871-102">Cenário de Publicação de Internet</span><span class="sxs-lookup"><span data-stu-id="4e871-102">Internet publishing scenario</span></span>

<span data-ttu-id="4e871-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e871-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4e871-p101">Este exemplo de código demonstra como usar o ADO com o Provedor DB Microsoft OLE para Publicação na Internet. Neste cenário, você criará um aplicativo do Visual Basic que usa os objetos **Recordset**, **Record** e **Stream** para exibir o conteúdo dos recursos publicados com o Internet Publishing Provider.</span><span class="sxs-lookup"><span data-stu-id="4e871-p101">This code example demonstrates how to use ADO with the Microsoft OLE DB Provider for Internet Publishing. In this scenario, you will create a Visual Basic application that uses **Recordset**, **Record**, and **Stream** objects to display the contents of resources published with the Internet Publishing Provider.</span></span>

<span data-ttu-id="4e871-106">As seguintes etapas são necessárias para criar este cenário:</span><span class="sxs-lookup"><span data-stu-id="4e871-106">The following steps are necessary to create this scenario:</span></span> 

1. <span data-ttu-id="4e871-107">Configure o projeto do Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4e871-107">Set up the Visual Basic project.</span></span>
2. <span data-ttu-id="4e871-108">Inicialize a caixa de listagem principal.</span><span class="sxs-lookup"><span data-stu-id="4e871-108">Initialize the Main list box.</span></span>
3. <span data-ttu-id="4e871-109">Preencha a caixa de lista de campos.</span><span class="sxs-lookup"><span data-stu-id="4e871-109">Populate the Fields list box.</span></span>
4. <span data-ttu-id="4e871-110">Preencha a caixa de texto de detalhes.</span><span class="sxs-lookup"><span data-stu-id="4e871-110">Populate the Details text box.</span></span>

## <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="4e871-111">Etapa 1: Configurar o projeto do Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4e871-111">Step 1: Set up the Visual Basic project</span></span>

<span data-ttu-id="4e871-112">Neste cenário, considera-se que você tem o Microsoft Visual Basic 6.0 ou posterior, ADO 2.5 ou posterior e o Microsoft OLE DB Provider for Internet Publishing instalado no seu sistema.</span><span class="sxs-lookup"><span data-stu-id="4e871-112">In this scenario, it is assumed that you have Microsoft Visual Basic 6.0 or later, ADO 2.5 or later, and the Microsoft OLE DB Provider for Internet Publishing installed on your system.</span></span>

### <a name="create-an-ado-project"></a><span data-ttu-id="4e871-113">Criar um projeto ADO</span><span class="sxs-lookup"><span data-stu-id="4e871-113">Create an ADO project</span></span>

1.  <span data-ttu-id="4e871-114">No Microsoft Visual Basic, crie um novo projeto EXE padrão.</span><span class="sxs-lookup"><span data-stu-id="4e871-114">In Microsoft Visual Basic, create a new Standard EXE project.</span></span>

2.  <span data-ttu-id="4e871-115">No menu **Projeto**, clique em **Referências**.</span><span class="sxs-lookup"><span data-stu-id="4e871-115">From the **Project** menu, choose **References**.</span></span>

3.  <span data-ttu-id="4e871-116">Selecione **Microsoft ActiveX Data Objects 2.5 Library**e, em seguida, clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="4e871-116">Select **Microsoft ActiveX Data Objects 2.5 Library**, and then click **OK**.</span></span>

### <a name="insert-controls-on-the-main-form"></a><span data-ttu-id="4e871-117">Inserir os controles no formulário principal</span><span class="sxs-lookup"><span data-stu-id="4e871-117">Insert controls on the main form</span></span>

1.  <span data-ttu-id="4e871-118">Adicione um controle ListBox em Form1.</span><span class="sxs-lookup"><span data-stu-id="4e871-118">Add a ListBox control to Form1.</span></span> <span data-ttu-id="4e871-119">Defina sua propriedade **Name** para **lstMain**.</span><span class="sxs-lookup"><span data-stu-id="4e871-119">Set its **Name** property to **lstMain**.</span></span>

2.  <span data-ttu-id="4e871-120">Adicione outro controle ListBox em Form1.</span><span class="sxs-lookup"><span data-stu-id="4e871-120">Add another ListBox control to Form1.</span></span> <span data-ttu-id="4e871-121">Defina sua propriedade **Name** para **lstDetails**.</span><span class="sxs-lookup"><span data-stu-id="4e871-121">Set its **Name** property to **lstDetails**.</span></span>

3.  <span data-ttu-id="4e871-122">Adicione um controle TextBox em Form1.</span><span class="sxs-lookup"><span data-stu-id="4e871-122">Add a TextBox control to Form1.</span></span> <span data-ttu-id="4e871-123">Defina sua propriedade **Name** para **txtDetails**.</span><span class="sxs-lookup"><span data-stu-id="4e871-123">Set its **Name** property to **txtDetails**.</span></span>

## <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="4e871-124">Etapa 2: Inicializar a caixa de listagem principal</span><span class="sxs-lookup"><span data-stu-id="4e871-124">Step 2: Initialize the Main list box</span></span>

### <a name="declare-global-record-and-recordset-objects"></a><span data-ttu-id="4e871-125">Declarar os objetos Record e Recordset globais</span><span class="sxs-lookup"><span data-stu-id="4e871-125">Declare global Record and Recordset objects</span></span>

- <span data-ttu-id="4e871-126">Insira o seguinte código em (General) (Declarations) para Form1:</span><span class="sxs-lookup"><span data-stu-id="4e871-126">Insert the following code into the (General) (Declarations) for Form1:</span></span>
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   <span data-ttu-id="4e871-127">Este código declara as referências de objetos globais para os objetos **Record** e **Recordset** que serão usados posteriormente neste cenário.</span><span class="sxs-lookup"><span data-stu-id="4e871-127">This code declares global object references for **Record** and **Recordset** objects that will be used later in this scenario.</span></span>

### <a name="connect-to-a-url-and-populate-lstmain"></a><span data-ttu-id="4e871-128">Conectar a uma URL e preencher lstMain</span><span class="sxs-lookup"><span data-stu-id="4e871-128">Connect to a URL and populate lstMain</span></span>

- <span data-ttu-id="4e871-129">Insira o seguinte código no manipulador de eventos Form Load para Form1:</span><span class="sxs-lookup"><span data-stu-id="4e871-129">Insert the following code into the Form Load event handler for Form1:</span></span>
    
   ```vb 
     
    Private Sub Form_Load() 
        Set grec = New Record 
        Set grs = New Recordset 
        grec.Open "", "URL=https://servername/foldername/", , _ 
            adOpenIfExists Or adCreateCollection 
        Set grs = grec.GetChildren 
        While Not grs.EOF 
            lstMain.AddItem grs(0) 
            grs.MoveNext 
        Wend 
    End Sub 
   ```
    
   <span data-ttu-id="4e871-130">Este código instancia os objetos **Record** e **Recordset** globais.</span><span class="sxs-lookup"><span data-stu-id="4e871-130">This code instantiates the global **Record** and **Recordset** objects.</span></span> <span data-ttu-id="4e871-131">O **registro** `grec` é aberta com uma URL especificada como o **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="4e871-131">The **Record** `grec` is opened with a URL specified as the **ActiveConnection**.</span></span> <span data-ttu-id="4e871-132">Se o URL existir, estará aberto; se ainda não existir, será criado.</span><span class="sxs-lookup"><span data-stu-id="4e871-132">If the URL exists, it is opened; if it does not already exist, it is created.</span></span> 
   
   <span data-ttu-id="4e871-133">Observe que você deve substituir `https://servername/foldername/` com uma URL válida do seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="4e871-133">Note that you should replace `https://servername/foldername/` with a valid URL from your environment.</span></span> 
   
   <span data-ttu-id="4e871-134">O **Recordset** `grs` é aberto no filho do **registro** `grec`.</span><span class="sxs-lookup"><span data-stu-id="4e871-134">The **Recordset** `grs` is opened on the children of the **Record** `grec`.</span></span> <span data-ttu-id="4e871-135">Então, o lstMain é preenchido com os nomes de arquivo dos recursos publicados no URL.</span><span class="sxs-lookup"><span data-stu-id="4e871-135">The lstMain is then populated with the file names of the resources published to the URL.</span></span>

## <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="4e871-136">Etapa 3: Preencher a caixa de lista de campos</span><span class="sxs-lookup"><span data-stu-id="4e871-136">Step 3: Populate the Fields list box</span></span>

- <span data-ttu-id="4e871-137">Insira o seguinte código no manipulador de eventos Click de lstMain:</span><span class="sxs-lookup"><span data-stu-id="4e871-137">Insert the following code into the Click event handler of lstMain:</span></span>

   ```vb 
    
    Private Sub lstMain_Click() 
        Dim rec As Record 
        Dim rs As Recordset 
        Set rec = New Record 
        Set rs = New Recordset 
        grs.MoveFirst 
        grs.Move lstMain.ListIndex 
        lstDetails.Clear 
        rec.Open grs 
        Select Case rec.RecordType 
            Case adCollectionRecord: 
                Set rs = rec.GetChildren 
                While Not rs.EOF 
                    lstDetails.AddItem rs(0) 
                    rs.MoveNext 
                Wend 
            Case adSimpleRecord: 
                recFields rec, lstDetails, txtDetails 
                
            Case adStructDoc: 
        End Select 
        
    End Sub 
   ```

   <span data-ttu-id="4e871-138">Este código declara e instancia os objetos **Record** e **Recordset** locais `rec` e `rs`respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4e871-138">This code declares and instantiates local **Record** and **Recordset** objects `rec` and `rs`respectively.</span></span>

   <span data-ttu-id="4e871-139">A linha correspondente ao recurso selecionado em lstMain é feita na linha atual de `grs`.</span><span class="sxs-lookup"><span data-stu-id="4e871-139">The row corresponding to the resource selected in lstMain is made the current row of `grs`.</span></span> <span data-ttu-id="4e871-140">Caixa de listagem **detalhes** é desmarcada, em seguida, e `rec` é aberto com a linha atual de `grs` como a fonte.</span><span class="sxs-lookup"><span data-stu-id="4e871-140">The **Details** list box is then cleared and `rec` is opened with the current row of `grs` as the source.</span></span>

   <span data-ttu-id="4e871-141">Se o recurso for um registro de coleção (conforme especificado por **RecordType**), o local **Recordset** `rs` é aberto no filho do `rec`.</span><span class="sxs-lookup"><span data-stu-id="4e871-141">If the resource is a collection record (as specified by **RecordType**), the local **Recordset** `rs` is opened on the children of `rec`.</span></span> <span data-ttu-id="4e871-142">em seguida, lstDetails é preenchido com os valores das linhas de `rs`.</span><span class="sxs-lookup"><span data-stu-id="4e871-142">lstDetails is then filled with the values from the rows of `rs`.</span></span>

   <span data-ttu-id="4e871-143">Se o recurso for um registro simple, `recFields` é chamado.</span><span class="sxs-lookup"><span data-stu-id="4e871-143">If the resource is a simple record, `recFields` is called.</span></span> <span data-ttu-id="4e871-144">Para obter mais informações sobre `recFields`, consulte a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="4e871-144">For more information about `recFields`, see the next step.</span></span>

   <span data-ttu-id="4e871-145">Nenhum código será implementado se o recurso for um documento estruturado.</span><span class="sxs-lookup"><span data-stu-id="4e871-145">No code is implemented if the resource is a structured document.</span></span>

## <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="4e871-146">Etapa 4: Preencher a caixa de texto detalhes</span><span class="sxs-lookup"><span data-stu-id="4e871-146">Step 4: Populate the Details text box</span></span>

- <span data-ttu-id="4e871-147">Criar uma nova sub-rotina chamada `recFields` e insira o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="4e871-147">Create a new subroutine named `recFields` and insert the following code:</span></span>

   ```vb 
    
    Sub recFields(r As Record, l As ListBox, t As TextBox) 
        Dim f As Field 
        Dim s As Stream 
        Set s = New Stream 
        Dim str As String 
        
        For Each f In r.Fields 
            l.AddItem f.Name & ": " & f.Value 
        Next 
        t.Text = "" 
        If r!RESOURCE_CONTENTCLASS = "text/plain" Then 
            s.Open r, adModeRead, adOpenStreamFromRecord 
            str = s.ReadText(1) 
            s.Position = 0 
            If Asc(Mid(str, 1, 1)) = 63 Then '//63 = "?" 
                s.Charset = "ascii" 
                s.Type = adTypeText 
            End If 
            t.Text = s.ReadText(adReadAll) 
        End If 
    End Sub 
   ```

   <span data-ttu-id="4e871-148">Este código preenche lstDetails com os campos e valores do registro simple passados para `recFields`.</span><span class="sxs-lookup"><span data-stu-id="4e871-148">This code populates lstDetails with the fields and values of the simple record passed to `recFields`.</span></span> <span data-ttu-id="4e871-149">Se o registro for um arquivo de texto, um texto **Stream** será aberto a partir do registro de recurso.</span><span class="sxs-lookup"><span data-stu-id="4e871-149">If the resource is a text file, a text **Stream** is opened from the resource record.</span></span> <span data-ttu-id="4e871-150">O código determina se o conjunto de caracteres ASCII e copia o conteúdo do **Stream** em `txtDetails`.</span><span class="sxs-lookup"><span data-stu-id="4e871-150">The code determines if the character set is ASCII, and copies the **Stream** contents into `txtDetails`.</span></span>

