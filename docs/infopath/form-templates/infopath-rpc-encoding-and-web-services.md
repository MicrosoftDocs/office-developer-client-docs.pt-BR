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
# <a name="infopath-rpc-encoding-and-web-services"></a>InfoPath, codificação RPC e serviços Web

Serviços Web podem expor um dos dois estilos de vinculação para os métodos Web no contrato do Web Service Description Language (WSDL) que descreve-los: documento ou RPC. Além disso, cada um desses dois estilos da associação pode ser especificado como um dos literal ou codificado. As implementações mais comuns para cada tipo são: documento/literal e RPC/codificado. No entanto, o Microsoft InfoPath suporta apenas se conectar aos serviços da Web que usam o estilo de documento/literal.
  
A maioria das ferramentas de desenvolvimento do serviço Web fornecem uma opção para especificar que tipo de serviço Web que você deseja criar. Se você estiver desenvolvendo um serviço Web que você se conectarão do InfoPath, você deve especificar o documento/literal como estilo e a codificação do serviço Web.
  
No entanto, se você não controlar o serviço Web que você deseja trabalhar com, e você deve se conectar a uma Web serviço usa o estilo RPC/codificado, você pode usar um serviço de proxy .NET para se conectar a um serviço Web RPC/codificado.
  
## <a name="using-a-net-proxy-service-to-connect-to-a-web-service"></a>Usando um serviço de Proxy .NET para se conectar a um serviço Web

Se você não controlar o serviço Web RPC/codificado que você deseja trabalhar com, você pode criar um proxy de documento/literal serviço Web do Microsoft .NET que fornece funções de wrapper para cada um dos métodos da Web, você deseja chamar do serviço da Web RPC/codificado. Em seguida, você pode trabalhar com o serviço Web do InfoPath de documento/literal do proxy.
  
Código do .NET framework pode trabalhar com qualquer tipo de serviço da Web (RPC/codificado e documento/literal) e todos os serviços .NET Web usam o documento/literal estilo e codificação. Porque o .NET Framework pode se comunicar com qualquer tipo de serviço da Web, você pode criar um serviço Web do .NET que tem métodos que fazer chamadas para o serviço Web RPC/codificado. O serviço Web do .NET irá atuar como um conversor que permite InfoPath fazer chamadas de estilo de documento/literal para o serviço Web do .NET que por sua vez, pode fazer chamadas de estilo RPC/codificado ao serviço da Web original.
  
Os pré-requisitos para a criação de tal um proxy de serviço Web do Microsoft .NET são um computador do Microsoft Windows ou o Microsoft Windows Server que está executando os serviços de informações da Internet (IIS) com instalado no qual você deseja implantar o proxy do serviço Web do ASP.NET. Quando você cria uma solução do InfoPath, você irá apontar para o proxy do serviço da Web, em vez do serviço Web RPC/codificado. O proxy do serviço Web, em seguida, fará chamadas para o serviço RPC/codificado.
  
## <a name="creating-a-proxy-web-service-using-visual-studio"></a>Criando um serviço Web de Proxy usando o Visual Studio

1. Crie um novo projeto de **Aplicativo de serviço de Web do ASP.NET** . 
    
2. No **Solution Explorer**, clique com botão direito na pasta de **referências** de seu novo projeto e clique em **Adicionar referência da Web**. 
    
3. Na caixa de diálogo **Adicionar referência da Web** , digite a URL do serviço Web RPC/codificado que você deseja trabalhar com e clique em **Ir**.
    
4. Clique em **Adicionar referência**. 
    
5. Abra o arquivo. asmx para seu serviço da Web e adicione um método de serviço Web para chamar cada método de serviço Web do serviço da Web RPC/codificado referenciado.
    
6. Para exibir uma lista dos métodos na referência do servidor Web RPC/codificado, exiba a janela de **Modo de exibição de classe** . Para cada método de serviço Web, você verá três métodos. Por exemplo, se o método de serviço Web é chamado `doSearch`, e em seguida, você verá três métodos chamados `doSearch`, `BegindoSearch`, e `EnddoSearch`. Você só precisa criar um método de serviço Web de wrapper para a `doSearch` método. Certifique-se de que correspondem a assinatura do método exato e tipo de retorno. 
    
7. Dentro de cada método de wrapper, é necessário escrever código para fazer uma chamada para o serviço Web RPC/codificado referenciado, conforme mostrado no exemplo a seguir. 
    
   ```cs
    [WebMethod] 
    public string[] doSearch(string keyword) 
    { 
        SearchService srch = new SearchService(); 
        return srch.doSearch(keyword); 
    } 
    
   ```

8. Se o serviço Web RPC/codificado requer autenticação, você pode codificar as credenciais necessárias para se conectar ao serviço Web RPC/codificado no código-fonte para o proxy do serviço Web do .NET ou você pode usar o código semelhante ao seguinte exemplo. 
    
   ```cs
    myProxy.Credentials = System.Net.CredentialCache.DefaultCredentials; 
    
   ```

Para obter mais informações, procure o artigo da Base de Conhecimento Microsoft "Como para: passar atual credenciais para um serviço da Web ASP.NET" em http://support.microsoft.com/.
    
## <a name="creating-a-proxy-web-service-without-visual-studio-net"></a>Criando um serviço Web de Proxy sem o Visual Studio .NET

Como alternativa, você pode criar um proxy de serviço da Web usando as ferramentas que são fornecidas com o .NET Framework Software Development Kit, que pode ser baixado do MSDN.
  
Use o Web Services Description Language Tool (Wsdl.exe) para criar o arquivo de código para seu proxy do serviço Web. Esse arquivo de código pode ser compilado usando o linha de comando compilador c# (csc.exe) ou o compilador de linha de comando de Visual Basic .NET (vbc.exe), que também são incluídos com o .NET Framework SDK. Depois que a ferramenta Web Services Description Language gerou o arquivo de código, renomeie a extensão de nome de arquivo para. asmx e abra o arquivo em qualquer editor de texto. Na primeira linha do documento, adicione a seguinte diretiva de página:
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
```

Vá até o final do arquivo de código e criar uma chamada para cada método de serviço Web no serviço Web RPC/codificado. O exemplo de código a seguir mostra o código para um serviço Web do .NET que se conecta ao serviço da Google Web, que usa o estilo de desenvolvimento do RPC/codificado. Há um espaço reservado para onde o código wsdl.exe gerado deve ir.
  
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


