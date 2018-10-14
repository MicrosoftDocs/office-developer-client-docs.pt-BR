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
# <a name="infopath-rpc-encoding-and-web-services"></a>InfoPath, codificação RPC e serviços Web

Serviços Web podem expor um dos dois estilos de associação para seus métodos Web no contrato da Linguagem de descrição de serviços Web(WSDL) que descreve: RPC ou documento. Além disso, cada um desses dois estilos de encadernação pode ser especificado como o literal ou codificado. Implementações mais comuns para cada tipo são: documento/caracteres literais e RPC/codificado. No entanto, o Microsoft InfoPath apenas dá suporte à conexão de serviços Web com o estilo de documento/literal.
  
A maioria das ferramentas de desenvolvimento do serviço Web fornecem uma opção para especificar o tipo de serviço Web que você deseja criar. Se você estiver desenvolvendo um serviço Web que se conectará ao InfoPath, você deve especificar e estilo do seu serviço Web como documento/literal como e a fazer a codificação.
  
No entanto, se você não domina o serviço Web que você deseja usar e precisa se conectar a um serviço Web, usando o estilo RPC/codificados, você pode usar o serviço de proxy do .NET para se conectar a um serviço Web RPC/codificado.
  
## <a name="using-a-net-proxy-service-to-connect-to-a-web-service"></a>Usar um serviço de Proxy .NET para se conectar a um serviço Web

Se você não domina o serviço Web RPC/codificação que você deseja usar, você pode criar um proxy de documento/literal de serviço Web do Microsoft .NET que fornece funções de conteúdo adicional para cada um dos métodos Web que você deseja invocar do serviço Web RPC/codificado. Você pode trabalhar com documentos proxy/literal de serviço Web do InfoPath.
  
O código .NET framework pode trabalhar com qualquer tipo de serviço Web (RPC/encoded e documento/literal) e todos os serviços Web do .NET usam o estilo e a codificação documento/literal. Como o .NET Framework pode se comunicar com qualquer tipo de serviço da Web, você pode criar um serviço Web com métodos para fazer o serviço Web RPC/codificado. O serviço Web .NET atuará como um tradutor que permite que o InfoPath faça chamadas do estilo documento/literal para o serviço da Web .NET, que por sua vez pode fazer chamadas com o estilo RPC/encoded estilo para o serviço Web original.
  
Os pré-requisitos para criar um proxy de serviço Web do Microsoft .NET são um computador Windows da Microsoft ou do Microsoft Windows Server com serviços de informações de Internet (IIS) instalado, onde será possível implantar o proxy de serviço Web do ASP.NET. Quando você cria uma solução do InfoPath, você apontará para o serviço Web proxy em vez do serviço Web RPC/encoded proxy. O proxy serviço da Web fará chamadas para o serviço RPC/encoded.
  
## <a name="creating-a-proxy-web-service-using-visual-studio"></a>Criar um serviço Web do Proxy usando o Visual Studio

1. Criar um novo projeto no **aplicativo de serviços Web ASP.NET**. 
    
2. No **Explorador de soluções**, clique com o botão direito em**referências** na pasta de novo projeto e clique em **adicionar referência Web**. 
    
3. Na caixa de diálogo**adicionar Web referência**, digite a URL do serviço Web RPC/codificação que você deseja usar e clique em **Ir**.
    
4. Clique em **adicionar referência**. 
    
5. Abra o arquivo. asmx para o seu serviço da Web e adicione um método de serviço Web para solicitar cada método de serviço Web usando o referenciado serviço Web RPC/encoded.
    
6. Para exibir uma lista dos métodos na referência do servidor Web RPC/codificados, exiba a janela **modo de exibição classe**. Para cada método de serviço Web, você verá três métodos. Por exemplo, se o método de serviço Web for acionado `doSearch`, em seguida, você verá três métodos chamados `doSearch`, `BegindoSearch`, e `EnddoSearch`. Você precisa criar um método de serviço Web de conteúdo adicional para o `doSearch` método. Certifique-se de combinar o método exato de assinatura com o tipo de retorno. 
    
7. Em cada método de conteúdo adicional, você precisa escrever o código para fazer uma chamada ao referenciado serviço Web RPC/encoded, conforme mostrado no exemplo a seguir. 
    
   ```cs
    [WebMethod] 
    public string[] doSearch(string keyword) 
    { 
        SearchService srch = new SearchService(); 
        return srch.doSearch(keyword); 
    } 
    
   ```

8. Se o serviço Web RPC/encoded requerer autenticação, codifique as credenciais necessárias para conectar o serviço Web RPC/encoded ao código fonte para o serviço Web .NET, ou então você pode usar um código como o do exemplo a seguir. 
    
   ```cs
    myProxy.Credentials = System.Net.CredentialCache.DefaultCredentials; 
    
   ```

Para saber mais, pesquise o artigo "Como: passar as credenciais atuais para um serviço da Web ASP.NET" na https://support.microsoft.com/.na Base de Dados de Conhecimento Microsoft
    
## <a name="creating-a-proxy-web-service-without-visual-studio-net"></a>Criar um serviço Web do Proxy sem usar o Visual Studio .NET

Como alternativa, você pode criar um proxy de serviço Web usando as ferramentas que são fornecidas com o .NET Framework SDK, que pode ser baixado no MSDN.
  
Use a ferramenta de idioma de descrição de serviços Web (Wsdl.exe) para criar o arquivo de código para o serviço Web proxy. Esse arquivo de código pode ser compilado usando a linha de comando compilador C# (csc.exe) ou o compilador de linha de comando .NET do Visual Basic (vbc.exe), que também está incluído no SDK do .NET Framework. Depois que a ferramenta de WSDL tiver gerado o arquivo de código, renomeie a extensão de nome de arquivo para. asmx e abra o arquivo em um editor de texto. Na primeira linha do documento, adicione a diretiva de página a seguir:
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
```

Vá até o final do arquivo de código para criar uma ligação para cada método de serviço Web no serviço Web RPC/codificado. O exemplo a seguir mostra o código de um serviço da Web que se conecta ao serviço Web do Google, que usa o estilo RPC/encoded de desenvolvimento. Há um espaço reservado para onde o código gerado wsdl.exe deve ir.
  
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


