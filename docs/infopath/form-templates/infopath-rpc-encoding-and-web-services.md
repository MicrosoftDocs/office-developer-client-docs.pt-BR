---
title: InfoPath, codificação RPC e serviços Web
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f8d7b944-a8fd-9c5f-8f66-0f1b628b7c6e
description: 'Serviços Web podem expor um dos dois estilos de vinculação para os métodos Web no contrato do Web Service Description Language (WSDL) que descreve-los: documento ou RPC.'
ms.openlocfilehash: 01b75df42bce97d62ebb5e273588cb522e5e2a09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765629"
---
# <a name="infopath-rpc-encoding-and-web-services"></a><span data-ttu-id="cc0d6-103">InfoPath, codificação RPC e serviços Web</span><span class="sxs-lookup"><span data-stu-id="cc0d6-103">InfoPath, RPC Encoding and Web Services</span></span>

<span data-ttu-id="cc0d6-104">Serviços Web podem expor um dos dois estilos de vinculação para os métodos Web no contrato do Web Service Description Language (WSDL) que descreve-los: documento ou RPC.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-104">Web services can expose one of two styles for binding to their Web methods in the Web Service Description Language (WSDL) contract that describes them: Document or RPC.</span></span> <span data-ttu-id="cc0d6-105">Além disso, cada um desses dois estilos da associação pode ser especificado como um dos literal ou codificado.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-105">Additionally, each of these two styles of binding can be specified as either literal or encoded.</span></span> <span data-ttu-id="cc0d6-106">As implementações mais comuns para cada tipo são: documento/literal e RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-106">The most common implementations for each type are: document/literal and RPC/encoded.</span></span> <span data-ttu-id="cc0d6-107">No entanto, o Microsoft InfoPath suporta apenas se conectar aos serviços da Web que usam o estilo de documento/literal.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-107">However, Microsoft InfoPath only supports connecting to Web services that use the document/literal style.</span></span>
  
<span data-ttu-id="cc0d6-108">A maioria das ferramentas de desenvolvimento do serviço Web fornecem uma opção para especificar que tipo de serviço Web que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-108">Most Web service development tools provide a switch for specifying what kind of Web service that you want to create.</span></span> <span data-ttu-id="cc0d6-109">Se você estiver desenvolvendo um serviço Web que você se conectarão do InfoPath, você deve especificar o documento/literal como estilo e a codificação do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-109">If you are developing a Web service that you will be connecting to from InfoPath, you should specify document/literal as your Web service's style and encoding.</span></span>
  
<span data-ttu-id="cc0d6-110">No entanto, se você não controlar o serviço Web que você deseja trabalhar com, e você deve se conectar a uma Web serviço usa o estilo RPC/codificado, você pode usar um serviço de proxy .NET para se conectar a um serviço Web RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-110">However, if you do not control the Web service that you want to work with, and you must connect to a Web service uses the RPC/encoded style, you can use a .NET proxy service to connect to an RPC/encoded Web service.</span></span>
  
## <a name="using-a-net-proxy-service-to-connect-to-a-web-service"></a><span data-ttu-id="cc0d6-111">Usando um serviço de Proxy .NET para se conectar a um serviço Web</span><span class="sxs-lookup"><span data-stu-id="cc0d6-111">Using a .NET Proxy Service to Connect to a Web Service</span></span>

<span data-ttu-id="cc0d6-112">Se você não controlar o serviço Web RPC/codificado que você deseja trabalhar com, você pode criar um proxy de documento/literal serviço Web do Microsoft .NET que fornece funções de wrapper para cada um dos métodos da Web, você deseja chamar do serviço da Web RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-112">If you do not control the RPC/encoded Web service that you want to work with, you can create a document/literal proxy Microsoft .NET Web service that provides wrapper functions for each of the Web methods, you want to invoke from the RPC/encoded Web service.</span></span> <span data-ttu-id="cc0d6-113">Em seguida, você pode trabalhar com o serviço Web do InfoPath de documento/literal do proxy.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-113">You can then work with the proxy document/literal Web service from InfoPath.</span></span>
  
<span data-ttu-id="cc0d6-114">Código do .NET framework pode trabalhar com qualquer tipo de serviço da Web (RPC/codificado e documento/literal) e todos os serviços .NET Web usam o documento/literal estilo e codificação.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-114">.NET Framework code can work with any kind of Web service (both RPC/encoded and document/literal), and all .NET Web services use the document/literal style and encoding.</span></span> <span data-ttu-id="cc0d6-115">Porque o .NET Framework pode se comunicar com qualquer tipo de serviço da Web, você pode criar um serviço Web do .NET que tem métodos que fazer chamadas para o serviço Web RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-115">Because the .NET Framework can communicate with any kind of Web service, you can create a .NET Web service that has methods that make calls to the RPC/encoded Web service.</span></span> <span data-ttu-id="cc0d6-116">O serviço Web do .NET irá atuar como um conversor que permite InfoPath fazer chamadas de estilo de documento/literal para o serviço Web do .NET que por sua vez, pode fazer chamadas de estilo RPC/codificado ao serviço da Web original.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-116">The .NET Web service will act as a translator that enables InfoPath to make document/literal style calls to the .NET Web service which in turn can make RPC/encoded style calls to the original Web service.</span></span>
  
<span data-ttu-id="cc0d6-117">Os pré-requisitos para a criação de tal um proxy de serviço Web do Microsoft .NET são um computador do Microsoft Windows ou o Microsoft Windows Server que está executando os serviços de informações da Internet (IIS) com instalado no qual você deseja implantar o proxy do serviço Web do ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-117">The prerequisites for creating such a proxy Microsoft .NET Web service are a Microsoft Windows or Microsoft Windows Server computer that is running Internet Information Services (IIS) with ASP.NET installed on which to deploy the proxy Web service.</span></span> <span data-ttu-id="cc0d6-118">Quando você cria uma solução do InfoPath, você irá apontar para o proxy do serviço da Web, em vez do serviço Web RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-118">When you create an InfoPath solution, you will point to the proxy Web service instead of the RPC/encoded Web service.</span></span> <span data-ttu-id="cc0d6-119">O proxy do serviço Web, em seguida, fará chamadas para o serviço RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-119">The proxy Web service will then make calls to the RPC/encoded service.</span></span>
  
## <a name="creating-a-proxy-web-service-using-visual-studio"></a><span data-ttu-id="cc0d6-120">Criando um serviço Web de Proxy usando o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cc0d6-120">Creating a Proxy Web Service Using Visual Studio</span></span>

1. <span data-ttu-id="cc0d6-121">Crie um novo projeto de **Aplicativo de serviço de Web do ASP.NET** .</span><span class="sxs-lookup"><span data-stu-id="cc0d6-121">Create a new **ASP.NET Web Service Application** project.</span></span> 
    
2. <span data-ttu-id="cc0d6-122">No **Solution Explorer**, clique com botão direito na pasta de **referências** de seu novo projeto e clique em **Adicionar referência da Web**.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-122">In the **Solution Explorer**, right-click the **References** folder of your new project, and then click **Add Web Reference**.</span></span> 
    
3. <span data-ttu-id="cc0d6-123">Na caixa de diálogo **Adicionar referência da Web** , digite a URL do serviço Web RPC/codificado que você deseja trabalhar com e clique em **Ir**.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-123">In the **Add Web Reference** dialog box, type in the URL of the RPC/encoded Web service that you want to work with, and then click **Go**.</span></span>
    
4. <span data-ttu-id="cc0d6-124">Clique em **Adicionar referência**.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-124">Click **Add Reference**.</span></span> 
    
5. <span data-ttu-id="cc0d6-125">Abra o arquivo. asmx para seu serviço da Web e adicione um método de serviço Web para chamar cada método de serviço Web do serviço da Web RPC/codificado referenciado.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-125">Open the .asmx file for your Web service and add one Web Service method to call each Web Service method from the referenced RPC/encoded Web service.</span></span>
    
6. <span data-ttu-id="cc0d6-126">Para exibir uma lista dos métodos na referência do servidor Web RPC/codificado, exiba a janela de **Modo de exibição de classe** .</span><span class="sxs-lookup"><span data-stu-id="cc0d6-126">To view a list of the methods in the reference RPC/encoded Web server, display the **Class View** window.</span></span> <span data-ttu-id="cc0d6-127">Para cada método de serviço Web, você verá três métodos.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-127">For each Web Service method, you will see three methods.</span></span> <span data-ttu-id="cc0d6-128">Por exemplo, se o método de serviço Web é chamado `doSearch`, e em seguida, você verá três métodos chamados `doSearch`, `BegindoSearch`, e `EnddoSearch`.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-128">For example, if the Web Service method is called  `doSearch`, then you will see three methods called  `doSearch`,  `BegindoSearch`, and  `EnddoSearch`.</span></span> <span data-ttu-id="cc0d6-129">Você só precisa criar um método de serviço Web de wrapper para a `doSearch` método.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-129">You only have to create a wrapper Web Service method for the  `doSearch` method.</span></span> <span data-ttu-id="cc0d6-130">Certifique-se de que correspondem a assinatura do método exato e tipo de retorno.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-130">Be sure to match the exact method signature and return type.</span></span> 
    
7. <span data-ttu-id="cc0d6-131">Dentro de cada método de wrapper, é necessário escrever código para fazer uma chamada para o serviço Web RPC/codificado referenciado, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-131">Within each wrapper method, you have to write code to make a call to the referenced RPC/encoded Web service as shown in the following example.</span></span> 
    
   ```cs
    [WebMethod] 
    public string[] doSearch(string keyword) 
    { 
        SearchService srch = new SearchService(); 
        return srch.doSearch(keyword); 
    } 
    
   ```

8. <span data-ttu-id="cc0d6-132">Se o serviço Web RPC/codificado requer autenticação, você pode codificar as credenciais necessárias para se conectar ao serviço Web RPC/codificado no código-fonte para o proxy do serviço Web do .NET ou você pode usar o código semelhante ao seguinte exemplo.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-132">If the RPC/encoded Web service requires authentication, you can hard code the credentials required to connect to the RPC/encoded Web service into the source code for the proxy .NET Web service, or you can use code like the following example.</span></span> 
    
   ```cs
    myProxy.Credentials = System.Net.CredentialCache.DefaultCredentials; 
    
   ```

<span data-ttu-id="cc0d6-133">Para obter mais informações, procure o artigo da Base de Conhecimento Microsoft "Como para: passar atual credenciais para um serviço da Web ASP.NET" em http://support.microsoft.com/.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-133">For more information, search for the Microsoft Knowledge Base article "HOW TO: Pass Current Credentials to an ASP.NET Web Service" on http://support.microsoft.com/.</span></span>
    
## <a name="creating-a-proxy-web-service-without-visual-studio-net"></a><span data-ttu-id="cc0d6-134">Criando um serviço Web de Proxy sem o Visual Studio .NET</span><span class="sxs-lookup"><span data-stu-id="cc0d6-134">Creating a Proxy Web Service Without Visual Studio .NET</span></span>

<span data-ttu-id="cc0d6-135">Como alternativa, você pode criar um proxy de serviço da Web usando as ferramentas que são fornecidas com o .NET Framework Software Development Kit, que pode ser baixado do MSDN.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-135">Alternatively, you can create a proxy Web service by using the tools that are provided with the .NET Framework Software Development Kit, which can be downloaded from MSDN.</span></span>
  
<span data-ttu-id="cc0d6-136">Use o Web Services Description Language Tool (Wsdl.exe) para criar o arquivo de código para seu proxy do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-136">Use the Web Services Description Language Tool (Wsdl.exe) to create the code file for your proxy Web service.</span></span> <span data-ttu-id="cc0d6-137">Esse arquivo de código pode ser compilado usando o linha de comando compilador c# (csc.exe) ou o compilador de linha de comando de Visual Basic .NET (vbc.exe), que também são incluídos com o .NET Framework SDK.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-137">This code file can be compiled by using the C# command-line compiler (csc.exe) or the Visual Basic .NET command-line compiler (vbc.exe), which are also included with the .NET Framework SDK.</span></span> <span data-ttu-id="cc0d6-138">Depois que a ferramenta Web Services Description Language gerou o arquivo de código, renomeie a extensão de nome de arquivo para. asmx e abra o arquivo em qualquer editor de texto.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-138">After the Web Services Description Language tool has generated the code file, rename the file name extension to .asmx and open the file in any text editor.</span></span> <span data-ttu-id="cc0d6-139">Na primeira linha do documento, adicione a seguinte diretiva de página:</span><span class="sxs-lookup"><span data-stu-id="cc0d6-139">On the very first line of the document, add the following page directive:</span></span>
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
```

<span data-ttu-id="cc0d6-140">Vá até o final do arquivo de código e criar uma chamada para cada método de serviço Web no serviço Web RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-140">Go to the end of the code file and create a call to each Web Service method in the RPC/encoded Web service.</span></span> <span data-ttu-id="cc0d6-141">O exemplo de código a seguir mostra o código para um serviço Web do .NET que se conecta ao serviço da Google Web, que usa o estilo de desenvolvimento do RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-141">The following code sample shows the code for a .NET Web service that connects to the Google Web service, which uses the RPC/encoded style of development.</span></span> <span data-ttu-id="cc0d6-142">Há um espaço reservado para onde o código wsdl.exe gerado deve ir.</span><span class="sxs-lookup"><span data-stu-id="cc0d6-142">There is a placeholder for where the wsdl.exe generated code should go.</span></span>
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
 
using System; 
using System.Web.Services; 
 
// The auto-generated code from the wsdl.exe tool goes here. 
 
[WebService] 
public class GoogleSearchServiceWrapper : System.Web.Services.WebService  
{ 
    [WebMethod] 
    public System.Byte[] doGetCachedPage(System.String key, System.String url) 
    { 
        GoogleSearchService srch = new GoogleSearchService(); 
        return srch.doGetCachedPage(key, url); 
    } 
 
    [WebMethod] 
    public System.String doSpellingSuggestion(System.String key, System.String phrase) 
    { 
        GoogleSearchService srch = new GoogleSearchService(); 
        return srch.doSpellingSuggestion(key, phrase); 
    } 
 
    [WebMethod] 
    public GoogleSearchResult doGoogleSearch(System.String key, 
      System.String q, 
      System.Int32 start, 
      System.Int32 maxResults, 
      System.Boolean filter, 
      System.String restrict, 
      System.Boolean safeSearch, 
      System.String lr, 
      System.String ie, 
      System.String oe) 
    {
        GoogleSearchService srch = new GoogleSearchService();
           return srch.doGoogleSearch(key, q, start, maxResults, 
               filter, restrict, safeSearch, lr, ie, oe); 
    } 
}
```


