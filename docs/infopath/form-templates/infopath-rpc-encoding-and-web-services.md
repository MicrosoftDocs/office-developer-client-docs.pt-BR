---
title: InfoPath, codificação RPC e serviços Web
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f8d7b944-a8fd-9c5f-8f66-0f1b628b7c6e
description: 'Serviços Web podem expor um dos dois estilos de associação para seus métodos Web no contrato da Linguagem de descrição de serviços Web(WSDL) que descreve: RPC ou documento.'
ms.openlocfilehash: 0eacf013c9cdf74f18f3de1d4412ca4ca165a960
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387675"
---
# <a name="infopath-rpc-encoding-and-web-services"></a><span data-ttu-id="aed24-103">InfoPath, codificação RPC e serviços Web</span><span class="sxs-lookup"><span data-stu-id="aed24-103">InfoPath, RPC Encoding and Web Services</span></span>

<span data-ttu-id="aed24-104">Serviços Web podem expor um dos dois estilos de associação para seus métodos Web no contrato da Linguagem de descrição de serviços Web(WSDL) que descreve: RPC ou documento.</span><span class="sxs-lookup"><span data-stu-id="aed24-104">Web services can expose one of two styles for binding to their Web methods in the Web Service Description Language (WSDL) contract that describes them: Document or RPC.</span></span> <span data-ttu-id="aed24-105">Além disso, cada um desses dois estilos de encadernação pode ser especificado como o literal ou codificado.</span><span class="sxs-lookup"><span data-stu-id="aed24-105">Additionally, each of these two styles of binding can be specified as either literal or encoded.</span></span> <span data-ttu-id="aed24-106">Implementações mais comuns para cada tipo são: documento/caracteres literais e RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="aed24-106">The most common implementations for each type are: document/literal and RPC/encoded.</span></span> <span data-ttu-id="aed24-107">No entanto, o Microsoft InfoPath apenas dá suporte à conexão de serviços Web com o estilo de documento/literal.</span><span class="sxs-lookup"><span data-stu-id="aed24-107">However, Microsoft InfoPath only supports connecting to Web services that use the document/literal style.</span></span>
  
<span data-ttu-id="aed24-108">A maioria das ferramentas de desenvolvimento do serviço Web fornecem uma opção para especificar o tipo de serviço Web que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="aed24-108">Most Web service development tools provide a switch for specifying what kind of Web service that you want to create.</span></span> <span data-ttu-id="aed24-109">Se você estiver desenvolvendo um serviço Web que se conectará ao InfoPath, você deve especificar e estilo do seu serviço Web como documento/literal como e a fazer a codificação.</span><span class="sxs-lookup"><span data-stu-id="aed24-109">If you are developing a Web service that you will be connecting to from InfoPath, you should specify document/literal as your Web service's style and encoding.</span></span>
  
<span data-ttu-id="aed24-110">No entanto, se você não domina o serviço Web que você deseja usar e precisa se conectar a um serviço Web, usando o estilo RPC/codificados, você pode usar o serviço de proxy do .NET para se conectar a um serviço Web RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="aed24-110">However, if you do not control the Web service that you want to work with, and you must connect to a Web service uses the RPC/encoded style, you can use a .NET proxy service to connect to an RPC/encoded Web service.</span></span>
  
## <a name="using-a-net-proxy-service-to-connect-to-a-web-service"></a><span data-ttu-id="aed24-111">Usar um serviço de Proxy .NET para se conectar a um serviço Web</span><span class="sxs-lookup"><span data-stu-id="aed24-111">Using a .NET Proxy Service to Connect to a Web Service</span></span>

<span data-ttu-id="aed24-112">Se você não domina o serviço Web RPC/codificação que você deseja usar, você pode criar um proxy de documento/literal de serviço Web do Microsoft .NET que fornece funções de conteúdo adicional para cada um dos métodos Web que você deseja invocar do serviço Web RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="aed24-112">If you do not control the RPC/encoded Web service that you want to work with, you can create a document/literal proxy Microsoft .NET Web service that provides wrapper functions for each of the Web methods, you want to invoke from the RPC/encoded Web service.</span></span> <span data-ttu-id="aed24-113">Você pode trabalhar com documentos proxy/literal de serviço Web do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="aed24-113">You can then work with the proxy document/literal Web service from InfoPath.</span></span>
  
<span data-ttu-id="aed24-114">O código .NET framework pode trabalhar com qualquer tipo de serviço Web (RPC/encoded e documento/literal) e todos os serviços Web do .NET usam o estilo e a codificação documento/literal.</span><span class="sxs-lookup"><span data-stu-id="aed24-114">.NET Framework code can work with any kind of Web service (both RPC/encoded and document/literal), and all .NET Web services use the document/literal style and encoding.</span></span> <span data-ttu-id="aed24-115">Como o .NET Framework pode se comunicar com qualquer tipo de serviço da Web, você pode criar um serviço Web com métodos para fazer o serviço Web RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="aed24-115">Because the .NET Framework can communicate with any kind of Web service, you can create a .NET Web service that has methods that make calls to the RPC/encoded Web service.</span></span> <span data-ttu-id="aed24-116">O serviço Web .NET atuará como um tradutor que permite que o InfoPath faça chamadas do estilo documento/literal para o serviço da Web .NET, que por sua vez pode fazer chamadas com o estilo RPC/encoded estilo para o serviço Web original.</span><span class="sxs-lookup"><span data-stu-id="aed24-116">The .NET Web service will act as a translator that enables InfoPath to make document/literal style calls to the .NET Web service which in turn can make RPC/encoded style calls to the original Web service.</span></span>
  
<span data-ttu-id="aed24-117">Os pré-requisitos para criar um proxy de serviço Web do Microsoft .NET são um computador Windows da Microsoft ou do Microsoft Windows Server com serviços de informações de Internet (IIS) instalado, onde será possível implantar o proxy de serviço Web do ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="aed24-117">The prerequisites for creating such a proxy Microsoft .NET Web service are a Microsoft Windows or Microsoft Windows Server computer that is running Internet Information Services (IIS) with ASP.NET installed on which to deploy the proxy Web service.</span></span> <span data-ttu-id="aed24-118">Quando você cria uma solução do InfoPath, você apontará para o serviço Web proxy em vez do serviço Web RPC/encoded proxy.</span><span class="sxs-lookup"><span data-stu-id="aed24-118">When you create an InfoPath solution, you will point to the proxy Web service instead of the RPC/encoded Web service.</span></span> <span data-ttu-id="aed24-119">O proxy serviço da Web fará chamadas para o serviço RPC/encoded.</span><span class="sxs-lookup"><span data-stu-id="aed24-119">The proxy Web service will then make calls to the RPC/encoded service.</span></span>
  
## <a name="creating-a-proxy-web-service-using-visual-studio"></a><span data-ttu-id="aed24-120">Criar um serviço Web do Proxy usando o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="aed24-120">Creating a Proxy Web Service Using Visual Studio</span></span>

1. <span data-ttu-id="aed24-121">Criar um novo projeto no **aplicativo de serviços Web ASP.NET**.</span><span class="sxs-lookup"><span data-stu-id="aed24-121">Create a new ASP.NET Web API project</span></span> 
    
2. <span data-ttu-id="aed24-122">No **Explorador de soluções**, clique com o botão direito em**referências** na pasta de novo projeto e clique em **adicionar referência Web**.</span><span class="sxs-lookup"><span data-stu-id="aed24-122">In the **Solution Explorer**, right-click the **References** folder of your new project, and then click **Add Web Reference**.</span></span> 
    
3. <span data-ttu-id="aed24-123">Na caixa de diálogo**adicionar Web referência**, digite a URL do serviço Web RPC/codificação que você deseja usar e clique em **Ir**.</span><span class="sxs-lookup"><span data-stu-id="aed24-123">In the **Add Web Reference** dialog box, type in the URL of the RPC/encoded Web service that you want to work with, and then click **Go**.</span></span>
    
4. <span data-ttu-id="aed24-124">Clique em **adicionar referência**.</span><span class="sxs-lookup"><span data-stu-id="aed24-124">Click **Add Reference**.</span></span> 
    
5. <span data-ttu-id="aed24-125">Abra o arquivo. asmx para o seu serviço da Web e adicione um método de serviço Web para solicitar cada método de serviço Web usando o referenciado serviço Web RPC/encoded.</span><span class="sxs-lookup"><span data-stu-id="aed24-125">Open the .asmx file for your Web service and add one Web Service method to call each Web Service method from the referenced RPC/encoded Web service.</span></span>
    
6. <span data-ttu-id="aed24-126">Para exibir uma lista dos métodos na referência do servidor Web RPC/codificados, exiba a janela **modo de exibição classe**.</span><span class="sxs-lookup"><span data-stu-id="aed24-126">To view a list of the methods in the reference RPC/encoded Web server, display the **Class View** window.</span></span> <span data-ttu-id="aed24-127">Para cada método de serviço Web, você verá três métodos.</span><span class="sxs-lookup"><span data-stu-id="aed24-127">For each Web Service method, you will see three methods.</span></span> <span data-ttu-id="aed24-128">Por exemplo, se o método de serviço Web for acionado `doSearch`, em seguida, você verá três métodos chamados `doSearch`, `BegindoSearch`, e `EnddoSearch`.</span><span class="sxs-lookup"><span data-stu-id="aed24-128">For example, if the Web Service method is called  `doSearch`, then you will see three methods called  `doSearch`,  `BegindoSearch`, and  `EnddoSearch`.</span></span> <span data-ttu-id="aed24-129">Você precisa criar um método de serviço Web de conteúdo adicional para o `doSearch` método.</span><span class="sxs-lookup"><span data-stu-id="aed24-129">You only have to create a wrapper Web Service method for the  `doSearch` method.</span></span> <span data-ttu-id="aed24-130">Certifique-se de combinar o método exato de assinatura com o tipo de retorno.</span><span class="sxs-lookup"><span data-stu-id="aed24-130">Be sure to match the exact method signature and return type.</span></span> 
    
7. <span data-ttu-id="aed24-131">Em cada método de conteúdo adicional, você precisa escrever o código para fazer uma chamada ao referenciado serviço Web RPC/encoded, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="aed24-131">Within each wrapper method, you have to write code to make a call to the referenced RPC/encoded Web service as shown in the following example.</span></span> 
    
   ```cs
    [WebMethod] 
    public string[] doSearch(string keyword) 
    { 
        SearchService srch = new SearchService(); 
        return srch.doSearch(keyword); 
    } 
    
   ```

8. <span data-ttu-id="aed24-132">Se o serviço Web RPC/encoded requerer autenticação, codifique as credenciais necessárias para conectar o serviço Web RPC/encoded ao código fonte para o serviço Web .NET, ou então você pode usar um código como o do exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="aed24-132">If the RPC/encoded Web service requires authentication, you can hard code the credentials required to connect to the RPC/encoded Web service into the source code for the proxy .NET Web service, or you can use code like the following example.</span></span> 
    
   ```cs
    myProxy.Credentials = System.Net.CredentialCache.DefaultCredentials; 
    
   ```

<span data-ttu-id="aed24-133">Para saber mais, pesquise o artigo "Como: passar as credenciais atuais para um serviço da Web ASP.NET" na https://support.microsoft.com/.na Base de Dados de Conhecimento Microsoft</span><span class="sxs-lookup"><span data-stu-id="aed24-133">For more information, search for the Microsoft Knowledge Base article "HOW TO: Pass Current Credentials to an ASP.NET Web Service" on https://support.microsoft.com/.</span></span>
    
## <a name="creating-a-proxy-web-service-without-visual-studio-net"></a><span data-ttu-id="aed24-134">Criar um serviço Web do Proxy sem usar o Visual Studio .NET</span><span class="sxs-lookup"><span data-stu-id="aed24-134">Creating a Proxy Web Service Without Visual Studio .NET</span></span>

<span data-ttu-id="aed24-135">Como alternativa, você pode criar um proxy de serviço Web usando as ferramentas que são fornecidas com o .NET Framework SDK, que pode ser baixado no MSDN.</span><span class="sxs-lookup"><span data-stu-id="aed24-135">Alternatively, you can create a proxy Web service by using the tools that are provided with the .NET Framework Software Development Kit, which can be downloaded from MSDN.</span></span>
  
<span data-ttu-id="aed24-136">Use a ferramenta de idioma de descrição de serviços Web (Wsdl.exe) para criar o arquivo de código para o serviço Web proxy.</span><span class="sxs-lookup"><span data-stu-id="aed24-136">Use the Web Services Description Language Tool (Wsdl.exe) to create the code file for your proxy Web service.</span></span> <span data-ttu-id="aed24-137">Esse arquivo de código pode ser compilado usando a linha de comando compilador C# (csc.exe) ou o compilador de linha de comando .NET do Visual Basic (vbc.exe), que também está incluído no SDK do .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="aed24-137">This code file can be compiled by using the C# command-line compiler (csc.exe) or the Visual Basic .NET command-line compiler (vbc.exe), which are also included with the .NET Framework SDK.</span></span> <span data-ttu-id="aed24-138">Depois que a ferramenta de WSDL tiver gerado o arquivo de código, renomeie a extensão de nome de arquivo para. asmx e abra o arquivo em um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="aed24-138">After the Web Services Description Language tool has generated the code file, rename the file name extension to .asmx and open the file in any text editor.</span></span> <span data-ttu-id="aed24-139">Na primeira linha do documento, adicione a diretiva de página a seguir:</span><span class="sxs-lookup"><span data-stu-id="aed24-139">On the very first line of the document, add the following page directive:</span></span>
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
```

<span data-ttu-id="aed24-140">Vá até o final do arquivo de código para criar uma ligação para cada método de serviço Web no serviço Web RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="aed24-140">Go to the end of the code file and create a call to each Web Service method in the RPC/encoded Web service.</span></span> <span data-ttu-id="aed24-141">O exemplo a seguir mostra o código de um serviço da Web que se conecta ao serviço Web do Google, que usa o estilo RPC/encoded de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="aed24-141">The following code sample shows the code for a .NET Web service that connects to the Google Web service, which uses the RPC/encoded style of development.</span></span> <span data-ttu-id="aed24-142">Há um espaço reservado para onde o código gerado wsdl.exe deve ir.</span><span class="sxs-lookup"><span data-stu-id="aed24-142">There is a placeholder for where the wsdl.exe generated code should go.</span></span>
  
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


