---
title: Esquemas de URI do Office
manager: luken
ms.date: 01/14/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ea99a8f-b005-4b92-b313-923294d20fbf
ms.openlocfilehash: 246c1da3647b61c6281c1a52a24826b3f22e5d7e
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293496"
---
# <a name="office-uri-schemes"></a><span data-ttu-id="66e4e-102">Esquemas de URI do Office</span><span class="sxs-lookup"><span data-stu-id="66e4e-102">Office URI Schemes</span></span>

## <a name="11-abstract"></a><span data-ttu-id="66e4e-103">1.1 RESUMO</span><span class="sxs-lookup"><span data-stu-id="66e4e-103">1.1 ABSTRACT</span></span>

<span data-ttu-id="66e4e-p101">Este documento define o formato de URIs (Uniform Resource Identifiers) para aplicativos de produtividade do escritório. O esquema tem suporte no Microsoft Office 2010 Service Pack 2 e posterior, incluindo o Microsoft Office 2013 para Windows e os produtos do Microsoft SharePoint 2013. Também tem suporte no Office for iPhone, Office for iPad e no Office for Mac 2011.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p101">This document defines the format of Uniform Resource Identifiers (URIs) for office productivity applications. The scheme is supported in Microsoft Office 2010 Service Pack 2 and later, including the Microsoft Office 2013 for Windows and the Microsoft SharePoint 2013 products. It is also supported in Office for iPhone, Office for iPad, and Office for Mac 2011.</span></span>
  
## <a name="12-introduction"></a><span data-ttu-id="66e4e-107">1.2 INTRODUÇÃO</span><span class="sxs-lookup"><span data-stu-id="66e4e-107">1.2 INTRODUCTION</span></span>

<span data-ttu-id="66e4e-p102">Estes esquemas de URI permitem que aplicativos de produtividade de escritório sejam chamados com vários comandos. Cada aplicativo recebe um esquema nomeado diferente, mas todos os esquemas seguem as mesmas regras para como a URI é formada (Esquema de URI).</span><span class="sxs-lookup"><span data-stu-id="66e4e-p102">These URI schemes allow for office productivity applications to be invoked with various commands. Each application is given a different named scheme but all schemes follow the same rules for how the URI is formed (URI Schema).</span></span>
  
## <a name="13-uri-schema"></a><span data-ttu-id="66e4e-110">1.3 ESQUEMA DE URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-110">1.3 URI SCHEMA</span></span>

### <a name="full-schema"></a><span data-ttu-id="66e4e-111">Esquema completo</span><span class="sxs-lookup"><span data-stu-id="66e4e-111">Full schema</span></span>

<span data-ttu-id="66e4e-112">< *scheme-name*  >:<  *command-name*  >"|"<  *command-argument-descriptor*  > "|"<  *command-argument*  ></span><span class="sxs-lookup"><span data-stu-id="66e4e-112">< *scheme-name*  >:<  *command-name*  >"|"<  *command-argument-descriptor*  > "|"<  *command-argument*  ></span></span> 
  
<span data-ttu-id="66e4e-p103">Uma URI como definida neste documento pode ter um ou mais argumentos de comando, cada um deve incluir os elementos < *descritor-command-argument*  > e <  *command-argument*  > e ser delimitada pelo caractere de barra vertical ("|"). Quando mais de um argumento de comando for incluído em uma URI, deverá haver um caractere de barra vertical ("|") separando cada argumento de comando do argumento de comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p103">A URI as defined in this document may have one or more command arguments, each of which must include both the < *command-argument-descriptor*  > and the <  *command-argument*  > elements and be delimited by the vertical bar ("|") character. When more than one command argument is included in a URI there must be a vertical bar ("|") character separating each command argument from the following command argument.</span></span> 
  
<span data-ttu-id="66e4e-p104">Esses esquemas não incluem um componente de autoridade como definido na seção 3.2 da RFC 3986. A invocação dos comandos especificados neste documento ocorre no contexto do sistema que está invocando o comando. Por exemplo, quando a URI "ms-excel:ofv|u|https://contoso/Q4/budget.xls" for invocada de um computador pessoal que esteja executando o Microsoft Windows com o Microsoft Office 2013 instalado, o resultado esperado é a instalação local do Microsoft Excel ser iniciada e os argumentos passados para abrir o arquivo em  *https://contoso/Q4/budget.xls*  em modo somente leitura. Observe que a barra vertical usada como um delimitador nesta especificação não está entre os caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente para maximizar o conjunto de caracteres com suporte do argumento do comando de URI sem a necessidade de codificar esses caracteres codificados por porcentagem.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p104">These schemes do not include an authority component as defined in section 3.2 of RFC 3986. Invocation of the commands specified in this document takes place in the context of the system invoking the command. For example, when the URI "ms-excel:ofv|u|https://contoso/Q4/budget.xls" is invoked from a personal computer running Microsoft Windows with Microsoft Office 2013 installed the expected result is that the local installation of Microsoft Excel will be launched and passed arguments to open the file at  *https://contoso/Q4/budget.xls*  in read-only mode. Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span> 
  
<span data-ttu-id="66e4e-120">A sintaxe do esquema inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="66e4e-120">The scheme syntax includes the following:</span></span>
  
1. <span data-ttu-id="66e4e-p105">< *scheme-name*  >: Isso se refere ao tipo de aplicativo que deve ser invocado. Por exemplo, o nome de esquema ms-word: está registrado pelo Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p105">< *scheme-name*  >: This refers to the type of application that should be invoked. For instance, the ms-word: scheme name is registered by Microsoft Word.</span></span> 
    
2. <span data-ttu-id="66e4e-123">Separador ":"</span><span class="sxs-lookup"><span data-stu-id="66e4e-123">":" separator</span></span>
    
3. <span data-ttu-id="66e4e-p106">< *command-name*  >: descreve as ações que o aplicativo deve executar. Por exemplo, a abertura de um documento para exibição. A lista de nomes de comando é descrita na seção 1.5.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p106">< *command-name*  >: This describes the actions that the application should perform. For instance, opening a document for viewing. The list of command names is described in section 1.5.</span></span> 
    
4. <span data-ttu-id="66e4e-127">Separador "|" (barra vertical)</span><span class="sxs-lookup"><span data-stu-id="66e4e-127">"|" (vertical bar) separator</span></span>
    
5. <span data-ttu-id="66e4e-128">< *command-argument-descriptor*  >: esse elemento oferece mais informações sobre o que argumento de comando trata.</span><span class="sxs-lookup"><span data-stu-id="66e4e-128">< *command-argument-descriptor*  >: This element gives more information about what the command argument is about.</span></span> 
    
6. <span data-ttu-id="66e4e-129">Separador "|" (barra vertical)</span><span class="sxs-lookup"><span data-stu-id="66e4e-129">"|" (vertical bar) separator</span></span>
    
7. <span data-ttu-id="66e4e-p107">< *command-argument*  >: os argumentos variam dependendo do comando. Um argumento comum é a URI para um documento tipicamente usando o esquema http ou https. Observe que, em segmentos <  *command-argument*  >, os caracteres reservados ":" e "/" da RFC 3986 fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p107">< *command-argument*  >: The arguments vary depending on the command. One common argument is the URI to a document, typically using the http or https scheme. Note that within <  *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
    
### <a name="abbreviated-schema"></a><span data-ttu-id="66e4e-133">Esquema abreviado</span><span class="sxs-lookup"><span data-stu-id="66e4e-133">Abbreviated schema</span></span>

<span data-ttu-id="66e4e-p108">Uma forma abreviada dos esquemas URI de escritório permite uma solicitação mais compacta para iniciar um aplicativo do Office especificado para abrir o recurso localizado em uma determinada URI. Essa forma abreviada implica no < *command-name*  > "ofv" e no <  *descritor-command-argument*  > "u". Nenhum outro controle ou argumentos de comando são permitidos neste esquema.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p108">An abbreviated form of the office URI schemes allows for a more compact request to launch a specified Office application to open the resource located at a given URI. This abbreviated form implies the < *command-name*  > "ofv" and the <  *command-argument-descriptor*  > "u". No further commands or command arguments are allowed in this schema.</span></span> 
  
<span data-ttu-id="66e4e-137">< *scheme-name*  >:<  *command-argument*  ></span><span class="sxs-lookup"><span data-stu-id="66e4e-137">< *scheme-name*  >:<  *command-argument*  ></span></span> 
  
1. <span data-ttu-id="66e4e-p109">< *scheme-name*  >: o tipo de aplicativo que deve ser invocado. Por exemplo, ms-word: para Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p109">< *scheme-name*  >: the type of application that should be invoked. For instance ms-word: for Microsoft Word.</span></span> 
    
2. <span data-ttu-id="66e4e-p110">< *command-argument*  >: URI para o recurso que o aplicativo deve abrir. Atualmente, somente URIs baseadas no esquema http ou https têm suporte.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p110">< *command-argument*  >: URI for the resource the application should open. Currently only URIs based on the http or https scheme are supported.</span></span> 
    
## <a name="14-scheme-names-and-office-application-registrations"></a><span data-ttu-id="66e4e-142">1.4 NOMES DE ESQUEMA E REGISTROS DE APLICATIVO DO OFFICE</span><span class="sxs-lookup"><span data-stu-id="66e4e-142">1.4 SCHEME NAMES AND OFFICE APPLICATION REGISTRATIONS</span></span>

<span data-ttu-id="66e4e-p111">A seguir, a lista de nomes de esquema implementados nos aplicativos do Microsoft Office. Quando o Microsoft Office estiver instalado, cada nome de esquema será registrado no Windows para ser manipulado pelo produto do Office do mesmo nome. Observe que "ms-spd" é uma abreviação de SharePoint Designer.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p111">The following is the list of scheme names implemented in Microsoft Office applications. When Microsoft Office is installed, each scheme name is registered with Windows to be handled by the Office product of the same name. Note that "ms-spd" is an abbreviation for SharePoint Designer.</span></span>
  
> - <span data-ttu-id="66e4e-146">*ms-word:*</span><span class="sxs-lookup"><span data-stu-id="66e4e-146">*ms-word:*</span></span> 
    
> - <span data-ttu-id="66e4e-147">*ms-powerpoint:*</span><span class="sxs-lookup"><span data-stu-id="66e4e-147">*ms-powerpoint:*</span></span> 
    
> - <span data-ttu-id="66e4e-148">*ms-excel:*</span><span class="sxs-lookup"><span data-stu-id="66e4e-148">*ms-excel:*</span></span> 
    
> - <span data-ttu-id="66e4e-149">*ms-visio:*</span><span class="sxs-lookup"><span data-stu-id="66e4e-149">*ms-visio:*</span></span> 
    
> - <span data-ttu-id="66e4e-150">*ms-access:*</span><span class="sxs-lookup"><span data-stu-id="66e4e-150">*ms-access:*</span></span> 
    
> - <span data-ttu-id="66e4e-151">*ms-project:*</span><span class="sxs-lookup"><span data-stu-id="66e4e-151">*ms-project:*</span></span> 
    
> - <span data-ttu-id="66e4e-152">*ms-publisher:*</span><span class="sxs-lookup"><span data-stu-id="66e4e-152">*ms-publisher:*</span></span> 
    
> - <span data-ttu-id="66e4e-153">*ms-spd:*</span><span class="sxs-lookup"><span data-stu-id="66e4e-153">*ms-spd:*</span></span> 
    
> - <span data-ttu-id="66e4e-154">*ms-infopath:*</span><span class="sxs-lookup"><span data-stu-id="66e4e-154">*ms-infopath:*</span></span> 
    
## <a name="15-commands-and-required-command-arguments"></a><span data-ttu-id="66e4e-155">1.5 COMANDOS E ARGUMENTOS DE COMANDO NECESSÁRIOS</span><span class="sxs-lookup"><span data-stu-id="66e4e-155">1.5 COMMANDS AND REQUIRED COMMAND ARGUMENTS</span></span>

### <a name="view-document"></a><span data-ttu-id="66e4e-156">Exibir Documento</span><span class="sxs-lookup"><span data-stu-id="66e4e-156">View Document</span></span>

<span data-ttu-id="66e4e-157">O comando a seguir fará com que o aplicativo abra o documento referenciado pela URI em um modo somente leitura ou de exibição.</span><span class="sxs-lookup"><span data-stu-id="66e4e-157">The following command will cause the application to open the document referenced by the URI in a read-only or view mode.</span></span>
  
> <span data-ttu-id="66e4e-158">Nome do comando: ofv</span><span class="sxs-lookup"><span data-stu-id="66e4e-158">Command Name: ofv</span></span>
    
> <span data-ttu-id="66e4e-159">Descritor de argumento de comando: u</span><span class="sxs-lookup"><span data-stu-id="66e4e-159">Command argument descriptor: u</span></span>
    
> <span data-ttu-id="66e4e-160">Argumento de comando: uma URI para o documento, com base no esquema http ou https</span><span class="sxs-lookup"><span data-stu-id="66e4e-160">Command argument: a URI to the document, based on the http or https scheme</span></span>
    
> <span data-ttu-id="66e4e-161">Exemplo:  *ms-excel:ofv|u|https://contoso/Q4/budget.xls*</span><span class="sxs-lookup"><span data-stu-id="66e4e-161">Example:  *ms-excel:ofv|u|https://contoso/Q4/budget.xls*</span></span> 
    
### <a name="edit-document"></a><span data-ttu-id="66e4e-162">Editar Documento</span><span class="sxs-lookup"><span data-stu-id="66e4e-162">Edit Document</span></span>

<span data-ttu-id="66e4e-163">O comando a seguir fará com que o aplicativo abra o documento referenciado pela URI em modo de edição.</span><span class="sxs-lookup"><span data-stu-id="66e4e-163">The following command will cause the application to open the document referenced by the URI in editing mode.</span></span>
  
> <span data-ttu-id="66e4e-164">Nome do comando: ofe</span><span class="sxs-lookup"><span data-stu-id="66e4e-164">Command Name: ofe</span></span>
    
> <span data-ttu-id="66e4e-165">Descritor de argumento de comando: u</span><span class="sxs-lookup"><span data-stu-id="66e4e-165">Command argument descriptor: u</span></span>
    
> <span data-ttu-id="66e4e-166">Argumento de comando: uma URI para o documento, com base no esquema http ou https</span><span class="sxs-lookup"><span data-stu-id="66e4e-166">Command argument: a URI to the document, based on the http or https scheme</span></span>
    
> <span data-ttu-id="66e4e-167">Exemplo:  *ms-powerpoint:ofe|u|https://www.fourthcoffee.com/AllHandsDeck.ppt*</span><span class="sxs-lookup"><span data-stu-id="66e4e-167">Example:  *ms-powerpoint:ofe|u|https://www.fourthcoffee.com/AllHandsDeck.ppt*</span></span> 
    
### <a name="new-document-from-template"></a><span data-ttu-id="66e4e-168">Novo Documento do Modelo</span><span class="sxs-lookup"><span data-stu-id="66e4e-168">New Document from Template</span></span>

<span data-ttu-id="66e4e-p112">O comando a seguir fará com que o aplicativo crie e abra um novo documento com base no modelo armazenado na URI especificada. O arquivo de modelo não é modificado nesse processo. Um argumento de comando adicional pode ser fornecido para especificar o caminho padrão oferecido como um local de salvamento quando o arquivo for salvo pela primeira vez. O usuário pode escolher uma localização diferente.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p112">The following command will cause the application to create and open a new document based on the template stored at the specified URI. The template file is not modified in this process. An additional command argument may be supplied to specify the default path offered as a save location when the file is first saved. It is possible for the user to choose a different location.</span></span>
  
> <span data-ttu-id="66e4e-173">Nome do comando: nft</span><span class="sxs-lookup"><span data-stu-id="66e4e-173">Command Name: nft</span></span>
    
> <span data-ttu-id="66e4e-174">Descritor de argumento de comando 1: u</span><span class="sxs-lookup"><span data-stu-id="66e4e-174">Command argument descriptor 1: u</span></span>
    
> <span data-ttu-id="66e4e-175">Argumento de comando 1: uma URI para o modelo, com base no esquema http ou https</span><span class="sxs-lookup"><span data-stu-id="66e4e-175">Command argument 1: a URI to the template, based on the http or https scheme</span></span>
    
> <span data-ttu-id="66e4e-176">Descritor de argumento de comando opcional 2: s</span><span class="sxs-lookup"><span data-stu-id="66e4e-176">Optional Command argument descriptor 2: s</span></span>
    
> <span data-ttu-id="66e4e-177">Argumento de comando opcional 2: URI para especificar a pasta de salvamento padrão</span><span class="sxs-lookup"><span data-stu-id="66e4e-177">Optional Command argument 2: URI to specify the default save folder</span></span>
    
> <span data-ttu-id="66e4e-178">Exemplo:  *ms-word:nft|u|https://cohowinery/templates/elegance.pot|s|https://cohowinery/presentations*</span><span class="sxs-lookup"><span data-stu-id="66e4e-178">Example:  *ms-word:nft|u|https://cohowinery/templates/elegance.pot|s|https://cohowinery/presentations*</span></span> 
    
<span data-ttu-id="66e4e-179">Como uma observação, se a localização de salvamento padrão opcional for fornecida, deve estar apontando para o mesmo nome de host como o modelo.</span><span class="sxs-lookup"><span data-stu-id="66e4e-179">As a note, if the optional default save location is supplied, it must be pointing to the same host name as the template.</span></span>
  
<span data-ttu-id="66e4e-180">Adicionalmente, os aplicativos SharePoint Designer e InfoPath (que implementa os esquemas ms-spd: e ms-infopath:, respectivamente) não dão suporte à funcionalidade "novo documento do modelo".</span><span class="sxs-lookup"><span data-stu-id="66e4e-180">Additionally, the SharePoint Designer and InfoPath applications (which implement the ms-spd: scheme and ms-infopath: schemes, respectively) do not support the "new document from template" functionality.</span></span>
  
## <a name="16-backwards-compatibility"></a><span data-ttu-id="66e4e-181">1.6 COMPATIBILIDADE COM VERSÕES ANTERIORES</span><span class="sxs-lookup"><span data-stu-id="66e4e-181">1.6 BACKWARDS COMPATIBILITY</span></span>

<span data-ttu-id="66e4e-p113">Ao analisar uma URI para extrair os argumentos de comando apropriados para um determinado comando, o manipulador de URI do Office só usará os argumentos de comando com o descritor de argumento de comando esperado. Se houver pares de argumentos e descritores de argumento adicionais com descritores de argumento inesperados, eles serão removidos da URI. Esse mecanismo permite que versões futuras do esquema adicionem argumentos de comando adicionais sem interromper a compatibilidade com versões anteriores com implementações legadas desse esquema.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p113">When parsing a URI to extract the appropriate command arguments for a given command, the Office URI handler will only use the command arguments that have the expected command argument descriptor. If there are additional pairs of arguments and argument descriptors that have unexpected argument descriptors, they will be removed from the URI. This mechanism allows future versions of the scheme to add additional command arguments without breaking backward compatibility with legacy implementations of this scheme.</span></span>
  
## <a name="17-implementation-restrictions-on-command-arguments"></a><span data-ttu-id="66e4e-185">1.7 RESTRIÇÕES DE IMPLEMENTAÇÃO SOBRE ARGUMENTOS DE COMANDO</span><span class="sxs-lookup"><span data-stu-id="66e4e-185">1.7 IMPLEMENTATION RESTRICTIONS ON COMMAND ARGUMENTS</span></span>

<span data-ttu-id="66e4e-186">As restrições abaixo são posicionadas em argumentos de comando em sua implementação atual no Office 2013.</span><span class="sxs-lookup"><span data-stu-id="66e4e-186">The below restrictions are placed on command arguments in its current implementation in Office 2013.</span></span>
  
### <a name="length-limitations-on-uri-command-arguments"></a><span data-ttu-id="66e4e-187">Limitações de tamanho em argumentos de comando de URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-187">Length limitations on URI command arguments</span></span>

<span data-ttu-id="66e4e-p114">Para argumentos de comando de URI, o tamanho máximo de caminho é de 256 caracteres para todos os aplicativos, exceto o Excel, onde o limite é 216. Tamanhos de caminho maiores do que esse podem ter suporte aplicativo por aplicativo e recomenda-se testar antes de implantar todas as soluções que utilizam isso.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p114">For URI command arguments, the maximum path length is 256 characters for all apps except Excel, where the limit is 216. Path lengths greater than these may be supported on an app-by-app basis and testing is recommended before deploying any solutions that rely on this.</span></span>
  
### <a name="allowed-characters-in-uri-command-arguments"></a><span data-ttu-id="66e4e-190">Caracteres permitidos em argumentos de comando de URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-190">Allowed characters in URI command arguments</span></span>

<span data-ttu-id="66e4e-191">UrIs permitidas devem estar em conformidade com os padrões propostos na RFC 3987 - Internationalized Resource Identifiers (IRIs) .</span><span class="sxs-lookup"><span data-stu-id="66e4e-191">Allowed URIs must conform to the standards proposed in RFC 3987 - Internationalized Resource Identifiers (IRIs) .</span></span> <span data-ttu-id="66e4e-192">Os caracteres identificados como reservados na RFC 3986 não devem ser codificados por porcentagem.</span><span class="sxs-lookup"><span data-stu-id="66e4e-192">Characters identified as reserved in RFC 3986 should not be percent encoded.</span></span> <span data-ttu-id="66e4e-193">.</span><span class="sxs-lookup"><span data-stu-id="66e4e-193">.</span></span> <span data-ttu-id="66e4e-194">Os nomes de arquivo não devem conter nenhum dos seguintes caracteres: \ / : ?</span><span class="sxs-lookup"><span data-stu-id="66e4e-194">Filenames must not contain any of the following characters: \ / : ?</span></span> <span data-ttu-id="66e4e-195">\< \> | " ou \* .</span><span class="sxs-lookup"><span data-stu-id="66e4e-195">\< \> | " or \*.</span></span>  
  
## <a name="appendix-a---uri-scheme-registration-template-for-ms-word-scheme"></a><span data-ttu-id="66e4e-196">APÊNDICE A - MODELO DE REGISTRO DE ESQUEMA URI PARA O ESQUEMA MS-WORD</span><span class="sxs-lookup"><span data-stu-id="66e4e-196">APPENDIX A - URI SCHEME REGISTRATION TEMPLATE FOR MS-WORD SCHEME</span></span>
<span data-ttu-id="66e4e-197"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="66e4e-197"><a name="bk_addresources"> </a></span></span>

### <a name="a-3-uri-scheme-syntax"></a><span data-ttu-id="66e4e-p116">A-3. Sintaxe do esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p116">A-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="66e4e-200">Esquema do Word = "ms-word:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="66e4e-200">Word Scheme = "ms-word:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="66e4e-201">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="66e4e-201">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="66e4e-202">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="66e4e-202">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="66e4e-203">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="66e4e-203">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="66e4e-204">document-uri = localização da URI de documento a ser aberto</span><span class="sxs-lookup"><span data-stu-id="66e4e-204">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="66e4e-205">template-uri = localização da URI de arquivo de modelo em que o novo arquivo se baseará</span><span class="sxs-lookup"><span data-stu-id="66e4e-205">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="66e4e-206">save-location = localização da URI da pasta em que o novo documento deve ser criado</span><span class="sxs-lookup"><span data-stu-id="66e4e-206">save-location = URI location of folder in which new document should be created</span></span>
    
### <a name="a-4-uri-scheme-semantics"></a><span data-ttu-id="66e4e-p117">A-4. Semântica do esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p117">A-4. URI Scheme Semantics</span></span>

<span data-ttu-id="66e4e-p118">O esquema ms-word define uma sintaxe de URI para abertura ou criação de um documento de processamento de texto. O esquema define três comandos que servem como instruções sobre o que deve ser feito com o documento referenciado. Os comandos são 1) open-for-edit-cmd (ofe), que instrui um aplicativo de processamento de texto a abrir o documento na URI especificada para edição; 2) open-for-view-cmd (ofv), que instrui um aplicativo de processamento de texto a abrir o documento na URI especificada em um modo somente leitura e 3) new-from-template-cmd (nft), que instrui um aplicativo de processamento de texto para criar um novo documento com base no modelo de documento localizado na URI template-uri especificada e salvar o novo documento na localização especificada na URI save-location opcional ou, na ausência dessa URI opcional, na localização da biblioteca de documentos padrão.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p118">The ms-word scheme defines a URI syntax for opening or creating a word processing document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a word processing application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a word processing application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a word processing application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="a-5-applicationsprotocols-that-use-the-ms-word-uri-scheme"></a><span data-ttu-id="66e4e-p119">A-5. Aplicativos/protocolos que usam o Esquema URI ms-word</span><span class="sxs-lookup"><span data-stu-id="66e4e-p119">A-5. Applications/Protocols that use the ms-word URI Scheme</span></span>

<span data-ttu-id="66e4e-p120">O Esquema URI ms-word URI é usado pelo Microsoft Office 2013 para invocar o Microsoft Word 2013 ou o Microsoft Word 2010 com Service Pack 2. O Microsoft SharePoint 2013 usa URIs ms-word como links para documentos de processamento de texto armazenados em bibliotecas de documentos do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p120">The ms-word URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Word 2013 or Microsoft Word 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-word URIs as links to word processing documents stored in SharePoint document libraries.</span></span>
  
### <a name="a-6-interoperability-considerations"></a><span data-ttu-id="66e4e-p121">A-6. Considerações sobre interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="66e4e-p121">A-6. Interoperability Considerations</span></span>

<span data-ttu-id="66e4e-p122">Observe que a barra vertical usada como um delimitador nesta especificação não está entre os caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente para maximizar o conjunto de caracteres com suporte do argumento do comando de URI sem a necessidade de codificar esses caracteres codificados por porcentagem.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p122">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters.. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="66e4e-220">Em segmentos < *command-argument*  >, os caracteres reservados da RFC 3986 ":" e "/" fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape.</span><span class="sxs-lookup"><span data-stu-id="66e4e-220">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="a-7-security-considerations"></a><span data-ttu-id="66e4e-p123">A-7. Considerações sobre segurança</span><span class="sxs-lookup"><span data-stu-id="66e4e-p123">A-7. Security Considerations</span></span>

 <span data-ttu-id="66e4e-p124">Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-word, clicar em um link para uma URI ms-word fará com que o aplicativo de processamento de texto registrado seja iniciado, com instruções para o aplicativo de processamento de texto tentar abrir um documento na URI especificada. Os aplicativos de processamento de texto que estejam se registrando para processar URIs ms-word devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p124">On systems that have registered handlers to recognize and act on ms-word URIs, clicking on a link to an ms-word URI will cause the registered word processing application to be launched, with instructions to the word processing application to attempt to open a document at the specified URI. Word processing applications registering to process ms-word URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span> 
  
### <a name="a-8-references"></a><span data-ttu-id="66e4e-p125">A-8. Referências</span><span class="sxs-lookup"><span data-stu-id="66e4e-p125">A-8. References</span></span>

<span data-ttu-id="66e4e-227">RFC 3987 \endash identificadores de recurso internacional (íris)</span><span class="sxs-lookup"><span data-stu-id="66e4e-227">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-b---uri-scheme-registration-template-for-ms-powerpoint-scheme"></a><span data-ttu-id="66e4e-228">APÊNDICE B - MODELO DE REGISTRO DE ESQUEMA URI PARA O ESQUEMA MS-POWERPOINT</span><span class="sxs-lookup"><span data-stu-id="66e4e-228">APPENDIX B - URI SCHEME REGISTRATION TEMPLATE FOR MS-POWERPOINT SCHEME</span></span>
<span data-ttu-id="66e4e-229"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="66e4e-229"><a name="bk_addresources"> </a></span></span>

### <a name="b-3-uri-scheme-syntax"></a><span data-ttu-id="66e4e-p126">B-3. Sintaxe do Esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p126">B-3. URI Scheme Syntax</span></span>

- <span data-ttu-id="66e4e-232">Esquema do PowerPoint = "ms-powerpoint:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="66e4e-232">PowerPoint Scheme = "ms-powerpoint:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
- <span data-ttu-id="66e4e-233">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="66e4e-233">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
- <span data-ttu-id="66e4e-234">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="66e4e-234">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
- <span data-ttu-id="66e4e-235">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="66e4e-235">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
- <span data-ttu-id="66e4e-236">document-uri = localização da URI de documento a ser aberto</span><span class="sxs-lookup"><span data-stu-id="66e4e-236">document-uri = URI location of document to open</span></span>
    
- <span data-ttu-id="66e4e-237">template-uri = localização da URI de arquivo de modelo em que o novo arquivo se baseará</span><span class="sxs-lookup"><span data-stu-id="66e4e-237">template-uri = URI location of template file upon which new file will be based</span></span>
    
- <span data-ttu-id="66e4e-238">save-location\* = localização da URI de pasta na qual o novo documento deve ser criado</span><span class="sxs-lookup"><span data-stu-id="66e4e-238">save-location\* = URI location of folder in which new document should be created</span></span>
    
- <span data-ttu-id="66e4e-239">\*save-location é um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="66e4e-239">\*save-location is an optional parameter</span></span>
    
### <a name="b-4-uri-scheme-semantics"></a><span data-ttu-id="66e4e-p127">B-4. Semântica do Esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p127">B-4. URI Scheme Semantics</span></span>

<span data-ttu-id="66e4e-p128">O esquema ms-powerpoint define uma sintaxe de URI para abertura ou criação de um documento de apresentação. O esquema define três comandos que servem como instruções sobre o que deve ser feito com o documento referenciado. Os comandos são 1) open-for-edit-cmd (ofe), que instrui um aplicativo de apresentação a abrir o documento na URI especificada para edição; 2) open-for-view-cmd (ofv), que instrui um aplicativo de apresentação a abrir o documento na URI especificada em um modo somente leitura e 3) new-from-template-cmd (nft), que instrui um aplicativo de apresentação para criar um novo documento com base no modelo de documento localizado na URI template-uri especificado e salvar o novo documento na localização especificada na URI save-location opcional ou, na ausência dessa URI opcional, na localização da biblioteca de documentos padrão.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p128">The ms-powerpoint scheme defines a URI syntax for opening or creating a presentation document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a presentation application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a presentation application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a presentation application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="b-5-applicationsprotocols-that-use-the-ms-powerpoint-uri-scheme"></a><span data-ttu-id="66e4e-p129">B-5. Aplicativos/protocolos que usam o Esquema URI ms-powerpoint</span><span class="sxs-lookup"><span data-stu-id="66e4e-p129">B-5. Applications/Protocols that use the ms-powerpoint URI Scheme</span></span>

<span data-ttu-id="66e4e-p130">O Esquema URI ms-powerpoint é usado pelo Microsoft Office 2013 para invocar o Microsoft PowerPoint 2013 ou o Microsoft PowerPoint 2010 com Service Pack 2. O Microsoft SharePoint 2013 usa URIs ms-powerpoint como links para documentos de apresentação armazenados em bibliotecas de documentos do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p130">The ms-powerpoint URI Scheme is used by Microsoft Office 2013 to invoke Microsoft PowerPoint 2013 or Microsoft PowerPoint 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-powerpoint URIs as links to presentation documents stored in SharePoint document libraries.</span></span>
  
### <a name="b-6-interoperability-considerations"></a><span data-ttu-id="66e4e-p131">B-6. Considerações sobre interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="66e4e-p131">B-6. Interoperability Considerations</span></span>

<span data-ttu-id="66e4e-p132">Observe que a barra vertical usada como um delimitador nesta especificação não está entre esses caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente, para maximizar o conjunto de caracteres que podem ter suporte do argumento do comando URI sem a necessidade de codificar esses caracteres como o símbolo de porcentagem.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p132">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="66e4e-253">Em segmentos < *command-argument*  >, os caracteres reservados da RFC 3986 ":" e "/" fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape.</span><span class="sxs-lookup"><span data-stu-id="66e4e-253">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="b-7-security-considerations"></a><span data-ttu-id="66e4e-p133">B-7. Considerações sobre segurança</span><span class="sxs-lookup"><span data-stu-id="66e4e-p133">B-7. Security Considerations</span></span>

<span data-ttu-id="66e4e-p134">Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-powerpoint, clicar em um link para uma URI ms-powerpoint fará com que o aplicativo de apresentação registrado seja iniciado, com instruções para o aplicativo de apresentação tentar abrir um documento na URI especificada. Os aplicativos de apresentação que estejam se registrando para processar URIs ms-powerpoint devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p134">On systems that have registered handlers to recognize and act on ms-powerpoint URIs, clicking on a link to an ms-powerpoint URI will cause the registered presentation application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-powerpoint URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="b-8-references"></a><span data-ttu-id="66e4e-p135">B-8. Referências</span><span class="sxs-lookup"><span data-stu-id="66e4e-p135">B-8. References</span></span>

<span data-ttu-id="66e4e-260">RFC 3987 \endash identificadores de recurso internacional (íris)</span><span class="sxs-lookup"><span data-stu-id="66e4e-260">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-c---uri-scheme-registration-template-for-ms-excel-scheme"></a><span data-ttu-id="66e4e-261">APÊNDICE C - MODELO DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-EXCEL</span><span class="sxs-lookup"><span data-stu-id="66e4e-261">APPENDIX C - URI SCHEME REGISTRATION TEMPLATE FOR MS-EXCEL SCHEME</span></span>
<span data-ttu-id="66e4e-262"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="66e4e-262"><a name="bk_addresources"> </a></span></span>

### <a name="c-3-uri-scheme-syntax"></a><span data-ttu-id="66e4e-p136">C-3. Sintaxe do Esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p136">C-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="66e4e-265">Esquema do Excel = "ms-excel:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="66e4e-265">Excel Scheme = "ms-excel:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="66e4e-266">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="66e4e-266">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="66e4e-267">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="66e4e-267">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="66e4e-268">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="66e4e-268">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="66e4e-269">document-uri = localização da URI de documento a ser aberto</span><span class="sxs-lookup"><span data-stu-id="66e4e-269">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="66e4e-270">template-uri = localização da URI de arquivo de modelo em que o novo arquivo se baseará</span><span class="sxs-lookup"><span data-stu-id="66e4e-270">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="66e4e-271">save-location\* = localização da URI de pasta na qual o novo documento deve ser criado</span><span class="sxs-lookup"><span data-stu-id="66e4e-271">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="66e4e-272">\*save-location é um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="66e4e-272">\*save-location is an optional parameter</span></span>
    
### <a name="c-4-uri-scheme-semantics"></a><span data-ttu-id="66e4e-p137">C-4. Semântica do Esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p137">C-4. URI Scheme Semantics</span></span>

<span data-ttu-id="66e4e-p138">O esquema ms-excel define uma sintaxe de URI para abertura ou criação de um documento de planilha. O esquema define três comandos que servem como instruções sobre o que deve ser feito com o documento referenciado. Os comandos são 1) open-for-edit-cmd (ofe), que instrui um aplicativo de planilha a abrir o documento na URI especificada para edição; 2) open-for-view-cmd (ofv), que instrui um aplicativo de planilha a abrir o documento na URI especificada em um modo somente leitura e 3) new-from-template-cmd (nft), que instrui um aplicativo de planilha para criar um novo documento com base no modelo de documento localizado na URI template-uri especificada e salvar o novo documento na localização especificada na URI save-location opcional ou, na ausência dessa URI opcional, na localização da biblioteca de documentos padrão.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p138">The ms-excel scheme defines a URI syntax for opening or creating a spreadsheet document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a spreadsheet application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a spreadsheet application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a spreadsheet application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="c-5-applicationsprotocols-that-use-the-ms-excel-uri-scheme"></a><span data-ttu-id="66e4e-p139">C-5. Aplicativos/protocolos que usam o Esquema URI ms-excel</span><span class="sxs-lookup"><span data-stu-id="66e4e-p139">C-5. Applications/Protocols that use the ms-excel URI Scheme</span></span>

<span data-ttu-id="66e4e-p140">O Esquema URI ms-excel é usado pelo Microsoft Office 2013 para invocar o Microsoft Excel 2013 ou o Microsoft Excel 2010 com Service Pack 2. O Microsoft SharePoint 2013 usa URIs ms-excel como links para documentos de planilha armazenados em bibliotecas de documentos do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p140">The ms-excel URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Excel 2013 or Microsoft Excel 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-excel URIs as links to spreadsheet documents stored in SharePoint document libraries.</span></span>
  
### <a name="c-6-interoperability-considerations"></a><span data-ttu-id="66e4e-p141">C-6. Considerações sobre interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="66e4e-p141">C-6. Interoperability Considerations</span></span>

<span data-ttu-id="66e4e-p142">Observe que a barra vertical usada como um delimitador nesta especificação não está entre esses caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente, para maximizar o conjunto de caracteres que podem ter suporte do argumento do comando URI sem a necessidade de codificar esses caracteres como o símbolo de porcentagem.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p142">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="66e4e-286">Em segmentos < *command-argument*  >, os caracteres reservados da RFC 3986 ":" e "/" fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape.</span><span class="sxs-lookup"><span data-stu-id="66e4e-286">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="c-7-security-considerations"></a><span data-ttu-id="66e4e-p143">C-7. Considerações sobre segurança</span><span class="sxs-lookup"><span data-stu-id="66e4e-p143">C-7. Security Considerations</span></span>

<span data-ttu-id="66e4e-p144">Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-excel, clicar em um link para uma URI ms-excel fará com que o aplicativo de planilha registrado seja iniciado, com instruções para o aplicativo tentar abrir um documento na URI especificada. Os aplicativos que estejam se registrando para processar URIs ms-excel devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p144">On systems that have registered handlers to recognize and act on ms-excel URIs, clicking on a link to an ms-excel URI will cause the registered spreadsheet application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-excel URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="c-8-references"></a><span data-ttu-id="66e4e-p145">C-8. Referências</span><span class="sxs-lookup"><span data-stu-id="66e4e-p145">C-8. References</span></span>

<span data-ttu-id="66e4e-293">RFC 3987 \endash identificadores de recurso internacional (íris)</span><span class="sxs-lookup"><span data-stu-id="66e4e-293">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-d---uri-scheme-registration-template-for-ms-visio-scheme"></a><span data-ttu-id="66e4e-294">APÊNDICE D - MODELO DE REGISTRO DE ESQUEMA URI PARA O ESQUEMA MS-VISIO</span><span class="sxs-lookup"><span data-stu-id="66e4e-294">APPENDIX D - URI SCHEME REGISTRATION TEMPLATE FOR MS-VISIO SCHEME</span></span>
<span data-ttu-id="66e4e-295"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="66e4e-295"><a name="bk_addresources"> </a></span></span>

### <a name="d-3-uri-scheme-syntax"></a><span data-ttu-id="66e4e-p146">D-3. Sintaxe do Esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p146">D-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="66e4e-298">Esquema do Visio = "ms-visio:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="66e4e-298">Visio Scheme = "ms-visio:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="66e4e-299">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="66e4e-299">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="66e4e-300">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="66e4e-300">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="66e4e-301">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="66e4e-301">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="66e4e-302">document-uri = localização da URI de documento a ser aberto</span><span class="sxs-lookup"><span data-stu-id="66e4e-302">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="66e4e-303">template-uri = localização da URI de arquivo de modelo em que o novo arquivo se baseará</span><span class="sxs-lookup"><span data-stu-id="66e4e-303">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="66e4e-304">save-location\* = localização da URI de pasta na qual o novo documento deve ser criado</span><span class="sxs-lookup"><span data-stu-id="66e4e-304">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="66e4e-305">\*save-location é um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="66e4e-305">\*save-location is an optional parameter</span></span>
    
### <a name="d-4-uri-scheme-semantics"></a><span data-ttu-id="66e4e-p147">D-4. Semântica do Esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p147">D-4. URI Scheme Semantics</span></span>

<span data-ttu-id="66e4e-p148">O esquema ms-visio define uma sintaxe de URI para abertura ou criação de um documento do Microsoft Visio. O esquema define três comandos que servem como instruções sobre o que deve ser feito com o documento referenciado. Os comandos são 1) open-for-edit-cmd (ofe), que instrui o Visio a abrir o documento na URI especificada para edição; 2) open-for-view-cmd (ofv), que instrui o Visio a abrir o documento na URI especificada em um modo somente leitura e 3) new-from-template-cmd (nft), que instrui o Visio a criar um novo documento com base no modelo de documento localizado na URI template-uri especificado e salvar o novo documento na localização especificada na URI save-location opcional ou, na ausência dessa URI opcional, na localização da biblioteca de documentos padrão.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p148">The ms-visio scheme defines a URI syntax for opening or creating a Microsoft Visio document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Visio to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Visio to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Visio to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="d-5-applicationsprotocols-that-use-the-ms-visio-uri-scheme"></a><span data-ttu-id="66e4e-p149">D-5. Aplicativos/protocolos que usam o Esquema URI ms-visio</span><span class="sxs-lookup"><span data-stu-id="66e4e-p149">D-5. Applications/Protocols that use the ms-visio URI Scheme</span></span>

<span data-ttu-id="66e4e-p150">O Esquema URI ms-visio é usado pelo Microsoft Office 2013 para invocar o Microsoft Visio 2013 ou o Microsoft Visio 2010 com Service Pack 2. O Microsoft SharePoint 2013 usa URIs ms-visio como links para documentos do Visio armazenados em bibliotecas de documentos do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p150">The ms-visio URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Visio 2013 or Microsoft Visio 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-visio URIs as links to Visio documents stored in SharePoint document libraries.</span></span>
  
### <a name="d-6-interoperability-considerations"></a><span data-ttu-id="66e4e-p151">D-6. Considerações sobre interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="66e4e-p151">D-6. Interoperability Considerations</span></span>

<span data-ttu-id="66e4e-p152">Observe que a barra vertical usada como um delimitador nesta especificação não está entre esses caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente, para maximizar o conjunto de caracteres que podem ter suporte do argumento do comando URI sem a necessidade de codificar esses caracteres como o símbolo de porcentagem.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p152">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="66e4e-319">Em segmentos < *command-argument*  >, os caracteres reservados da RFC 3986 ":" e "/" fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape.</span><span class="sxs-lookup"><span data-stu-id="66e4e-319">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="d-7-security-considerations"></a><span data-ttu-id="66e4e-p153">D-7. Considerações sobre segurança</span><span class="sxs-lookup"><span data-stu-id="66e4e-p153">D-7. Security Considerations</span></span>

<span data-ttu-id="66e4e-p154">Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-visio, clicar em um link para uma URI ms-visio fará com que o aplicativo registrado seja iniciado, com instruções para o aplicativo tentar abrir um documento na URI especificada. Os aplicativos que estejam se registrando para processar URIs ms-visio devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p154">On systems that have registered handlers to recognize and act on ms-visio URIs, clicking on a link to an ms-visio URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-visio URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="d-8-references"></a><span data-ttu-id="66e4e-p155">D-8. Referências</span><span class="sxs-lookup"><span data-stu-id="66e4e-p155">D-8. References</span></span>

<span data-ttu-id="66e4e-326">RFC 3987 \endash identificadores de recurso internacional (íris)</span><span class="sxs-lookup"><span data-stu-id="66e4e-326">RFC 3987 - International Resource Identifiers (IRIs)</span></span>
  
## <a name="appendix-e---uri-scheme-registration-template-for-ms-access-scheme"></a><span data-ttu-id="66e4e-327">APÊNDICE E - MODELO DE REGISTRO DE ESQUEMA URI PARA O ESQUEMA MS-ACCESS</span><span class="sxs-lookup"><span data-stu-id="66e4e-327">APPENDIX E - URI SCHEME REGISTRATION TEMPLATE FOR MS-ACCESS SCHEME</span></span>
<span data-ttu-id="66e4e-328"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="66e4e-328"><a name="bk_addresources"> </a></span></span>

### <a name="e-3-uri-scheme-syntax"></a><span data-ttu-id="66e4e-p156">E-3. Sintaxe do Esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p156">E-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="66e4e-331">Esquema do Access = "ms-access:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="66e4e-331">Access Scheme = "ms-access:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="66e4e-332">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="66e4e-332">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="66e4e-333">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="66e4e-333">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="66e4e-334">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="66e4e-334">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="66e4e-335">document-uri = localização da URI de documento a ser aberto</span><span class="sxs-lookup"><span data-stu-id="66e4e-335">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="66e4e-336">template-uri = localização da URI de arquivo de modelo em que o novo arquivo se baseará</span><span class="sxs-lookup"><span data-stu-id="66e4e-336">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="66e4e-337">save-location\* = localização da URI de pasta na qual o novo documento deve ser criado</span><span class="sxs-lookup"><span data-stu-id="66e4e-337">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="66e4e-338">\*save-location é um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="66e4e-338">\*save-location is an optional parameter</span></span>
    
### <a name="e-4-uri-scheme-semantics"></a><span data-ttu-id="66e4e-p157">E-4. Semântica do Esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p157">E-4. URI Scheme Semantics</span></span>

<span data-ttu-id="66e4e-p158">O esquema ms-access define uma sintaxe de URI para abertura ou criação de um banco de dados. O esquema define três comandos que servem como instruções sobre o que deve ser feito com o arquivo de banco de dados referenciado. Os comandos são 1) open-for-edit-cmd (ofe), que instrui o aplicativo de banco de dados a abrir o documento na URI especificada para edição; 2) open-for-view-cmd (ofv), que instrui o aplicativo de banco de dados a abrir o documento na URI especificada em um modo somente leitura e 3) new-from-template-cmd (nft), que instrui o aplicativo de banco de dados a criar um novo documento com base no modelo de documento localizado na URI template-uri especificado e salvar o novo banco de dados na localização especificada na URI save-location opcional ou, na ausência dessa URI opcional, na localização da biblioteca de documentos padrão.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p158">The ms-access scheme defines a URI syntax for opening or creating a database. The scheme defines three commands that serve as instructions regarding what should be done with the referenced database file. The commands are 1) open-for-edit-cmd (ofe), which instructs the database application to open the database at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs the database application to open the database at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs the database application to create a new database based on the template located at the specified template-uri URI and save the new database either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="e-5-applicationsprotocols-that-use-the-ms-access-uri-scheme"></a><span data-ttu-id="66e4e-p159">E-5. Aplicativos/protocolos que usam o Esquema URI ms-access</span><span class="sxs-lookup"><span data-stu-id="66e4e-p159">E-5. Applications/Protocols that use the ms-access URI Scheme</span></span>

<span data-ttu-id="66e4e-p160">O Esquema URI ms-access é usado pelo Microsoft Office 2013 para invocar o Microsoft Access 2013 ou o Microsoft Access 2010 com Service Pack 2 de páginas da Web. O Microsoft SharePoint 2013 usa URIs ms-access como links para bancos de dados do Access armazenados em bibliotecas de documentos do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p160">The ms-access URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Access 2013 or Microsoft Access 2010 with Service Pack 2 from web pages. Microsoft SharePoint 2013 uses ms-access URIs as links to Access databases stored in SharePoint document libraries.</span></span>
  
### <a name="e-6-interoperability-considerations"></a><span data-ttu-id="66e4e-p161">E-6. Considerações sobre interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="66e4e-p161">E-6. Interoperability Considerations</span></span>

<span data-ttu-id="66e4e-350">Observe que a barra vertical usada como um delimitador nesta especificação não está entre esses caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores.</span><span class="sxs-lookup"><span data-stu-id="66e4e-350">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters.</span></span> <span data-ttu-id="66e4e-351">Isso é feito intencionalmente, para maximizar o conjunto de caracteres que podem ter suporte do argumento do comando URI sem a necessidade de codificar esses caracteres como o símbolo de porcentagem.</span><span class="sxs-lookup"><span data-stu-id="66e4e-351">This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span> <span data-ttu-id="66e4e-352">Dentro \<command-argument\> de segmentos, os caracteres reservados RFC 3986 ":" e "/" fazem parte dos dados do argumento, não delimitadores e, portanto, são incluídos sem proteção.</span><span class="sxs-lookup"><span data-stu-id="66e4e-352">Within \<command-argument\> segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span>
  
### <a name="e-7-security-considerations"></a><span data-ttu-id="66e4e-p163">E-7. Considerações sobre segurança</span><span class="sxs-lookup"><span data-stu-id="66e4e-p163">E-7. Security Considerations</span></span>

<span data-ttu-id="66e4e-p164">Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-access, clicar em um link para uma URI ms-access fará com que o aplicativo registrado seja iniciado, com instruções para o aplicativo tentar abrir um banco de dados na URI especificada. Os aplicativos que estejam se registrando para processar URIs ms-access devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p164">On systems that have registered handlers to recognize and act on ms-access URIs, clicking on a link to an ms-access URI will cause the registered application to be launched, with instructions to the application to attempt to open a database at the specified URI. Applications registering to process ms-access URIs should implement protections to guard against opening databases from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="e-8-references"></a><span data-ttu-id="66e4e-p165">E-8. Referências</span><span class="sxs-lookup"><span data-stu-id="66e4e-p165">E-8. References</span></span>

<span data-ttu-id="66e4e-359">RFC 3987 \endash identificadores de recurso internacional (íris)</span><span class="sxs-lookup"><span data-stu-id="66e4e-359">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-f---uri-scheme-registration-template-for-ms-project-scheme"></a><span data-ttu-id="66e4e-360">APÊNDICE F - MODELO DE REGISTRO DE ESQUEMA URI PARA O ESQUEMA MS-PROJECT</span><span class="sxs-lookup"><span data-stu-id="66e4e-360">APPENDIX F - URI SCHEME REGISTRATION TEMPLATE FOR MS-PROJECT SCHEME</span></span>
<span data-ttu-id="66e4e-361"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="66e4e-361"><a name="bk_addresources"> </a></span></span>

### <a name="f-3-uri-scheme-syntax"></a><span data-ttu-id="66e4e-p166">F-3. Sintaxe do Esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p166">F-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="66e4e-364">Esquema do Project = "ms-project:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="66e4e-364">Project Scheme = "ms-project:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="66e4e-365">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="66e4e-365">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="66e4e-366">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="66e4e-366">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="66e4e-367">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="66e4e-367">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="66e4e-368">document-uri = localização da URI de documento a ser aberto</span><span class="sxs-lookup"><span data-stu-id="66e4e-368">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="66e4e-369">template-uri = localização da URI de arquivo de modelo em que o novo arquivo se baseará</span><span class="sxs-lookup"><span data-stu-id="66e4e-369">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="66e4e-370">save-location\* = localização da URI de pasta na qual o novo documento deve ser criado</span><span class="sxs-lookup"><span data-stu-id="66e4e-370">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="66e4e-371">\*save-location é um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="66e4e-371">\*save-location is an optional parameter</span></span>
    
### <a name="f-4-uri-scheme-semantics"></a><span data-ttu-id="66e4e-p167">F-4. Semântica do Esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p167">F-4. URI Scheme Semantics</span></span>

<span data-ttu-id="66e4e-p168">O esquema ms-project define uma sintaxe de URI para abertura ou criação de um documento do Microsoft Project. O esquema define três comandos que servem como instruções sobre o que deve ser feito com o documento referenciado. Os comandos são 1) open-for-edit-cmd (ofe), que instrui o Project a abrir o documento na URI especificada para edição; 2) open-for-view-cmd (ofv), que instrui o Project a abrir o documento na URI especificada em um modo somente leitura e 3) new-from-template-cmd (nft), que instrui o Project para criar um novo documento com base no modelo de documento localizado na URI template-uri especificado e salvar o novo documento na localização especificada na URI save-location opcional ou, na ausência dessa URI opcional, na localização da biblioteca de documentos padrão.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p168">The ms-project scheme defines a URI syntax for opening or creating a Microsoft Project document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Project to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Project to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Project to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="f-5-applicationsprotocols-that-use-the-ms-project-uri-scheme"></a><span data-ttu-id="66e4e-p169">F-5. Aplicativos/protocolos que usam o Esquema URI ms-project</span><span class="sxs-lookup"><span data-stu-id="66e4e-p169">F-5. Applications/Protocols that use the ms-project URI Scheme</span></span>

<span data-ttu-id="66e4e-p170">O Esquema URI ms-project é usado pelo Microsoft Office 2013 para invocar o Microsoft Project 2013 de páginas da Web. O Microsoft SharePoint 2013 usa URIs ms-project como links para documentos do Project armazenados em bibliotecas de documentos do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p170">The ms-project URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Project 2013 from web pages. Microsoft SharePoint 2013 uses ms-project URIs as links to Project documents stored in SharePoint document libraries.</span></span>
  
### <a name="f-6-interoperability-considerations"></a><span data-ttu-id="66e4e-p171">F-6. Considerações sobre interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="66e4e-p171">F-6. Interoperability Considerations</span></span>

<span data-ttu-id="66e4e-p172">Observe que a barra vertical usada como um delimitador nesta especificação não está entre esses caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente, para maximizar o conjunto de caracteres que podem ter suporte do argumento do comando URI sem a necessidade de codificar esses caracteres como o símbolo de porcentagem.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p172">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="66e4e-385">Em segmentos < *command-argument*  >, os caracteres reservados da RFC 3986 ":" e "/" fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape.</span><span class="sxs-lookup"><span data-stu-id="66e4e-385">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="f-7-security-considerations"></a><span data-ttu-id="66e4e-p173">F-7. Considerações sobre segurança</span><span class="sxs-lookup"><span data-stu-id="66e4e-p173">F-7. Security Considerations</span></span>

<span data-ttu-id="66e4e-p174">Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-project, clicar em um link para uma URI ms-project fará com que o aplicativo registrado seja iniciado, com instruções para o aplicativo tentar abrir um documento na URI especificada. Os aplicativos que estejam se registrando para processar URIs ms-project devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p174">On systems that have registered handlers to recognize and act on ms-project URIs, clicking on a link to an ms-project URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-project URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="f-8-references"></a><span data-ttu-id="66e4e-p175">F-8. Referências</span><span class="sxs-lookup"><span data-stu-id="66e4e-p175">F-8. References</span></span>

<span data-ttu-id="66e4e-392">RFC 3987 \endash identificadores de recurso internacional (íris)</span><span class="sxs-lookup"><span data-stu-id="66e4e-392">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-g---uri-scheme-registration-template-for-ms-publisher-scheme"></a><span data-ttu-id="66e4e-393">APÊNDICE G - MODELO DE REGISTRO DE ESQUEMA URI PARA O ESQUEMA MS-PUBLISHER</span><span class="sxs-lookup"><span data-stu-id="66e4e-393">APPENDIX G - URI SCHEME REGISTRATION TEMPLATE FOR MS-PUBLISHER SCHEME</span></span>
<span data-ttu-id="66e4e-394"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="66e4e-394"><a name="bk_addresources"> </a></span></span>

### <a name="g-3-uri-scheme"></a><span data-ttu-id="66e4e-p176">G-3. Esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p176">G-3. URI Scheme</span></span>

> <span data-ttu-id="66e4e-397">Sintaxe Esquema do Publisher = "ms-publisher:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="66e4e-397">Syntax Publisher Scheme = "ms-publisher:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="66e4e-398">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="66e4e-398">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="66e4e-399">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="66e4e-399">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="66e4e-400">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="66e4e-400">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="66e4e-401">document-uri = localização da URI de documento a ser aberto</span><span class="sxs-lookup"><span data-stu-id="66e4e-401">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="66e4e-402">template-uri = localização da URI de arquivo de modelo em que o novo arquivo se baseará</span><span class="sxs-lookup"><span data-stu-id="66e4e-402">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="66e4e-403">save-location\* = localização da URI de pasta na qual o novo documento deve ser criado</span><span class="sxs-lookup"><span data-stu-id="66e4e-403">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="66e4e-404">\*save-location é um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="66e4e-404">\*save-location is an optional parameter</span></span>
    
### <a name="g-4-uri-scheme-semantics"></a><span data-ttu-id="66e4e-p177">G-4. Semântica do Esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p177">G-4. URI Scheme Semantics</span></span>

<span data-ttu-id="66e4e-p178">O esquema ms-publisher define uma sintaxe de URI para abertura ou criação de um documento do Microsoft Publisher. O esquema define três comandos que servem como instruções sobre o que deve ser feito com o documento referenciado. Os comandos são 1) open-for-edit-cmd (ofe), que instrui o Publisher a abrir o documento na URI especificada para edição; 2) open-for-view-cmd (ofv), que instrui o Publisher a abrir o documento na URI especificada em um modo somente leitura e 3) new-from-template-cmd (nft), que instrui o Publisher para criar um novo documento com base no modelo de documento localizado na URI template-uri especificada e salvar o novo documento na localização especificada na URI save-location opcional ou, na ausência dessa URI opcional, na localização da biblioteca de documentos padrão.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p178">The ms-publisher scheme defines a URI syntax for opening or creating a Microsoft Publisher document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Publisher to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Publisher to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Publisher to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="g-5-applicationsprotocols-that-use-the-ms-publisher-uri-scheme"></a><span data-ttu-id="66e4e-p179">G-5. Aplicativos/protocolos que usam o Esquema URI ms-publisher</span><span class="sxs-lookup"><span data-stu-id="66e4e-p179">G-5. Applications/Protocols that use the ms-publisher URI Scheme</span></span>

<span data-ttu-id="66e4e-p180">O Esquema URI ms-publisher é usado pelo Microsoft Office 2013 para invocar o Microsoft Publisher 2013 ou o Microsoft Publisher 2010 com Service Pack 2 de páginas da Web. O Microsoft SharePoint 2013 usa URIs ms-publisher como links para documentos do Publisher armazenados em bibliotecas de documentos do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p180">The ms-publisher URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Publisher 2013 or Microsoft Publisher 2010 with Service Pack 2 from web pages. Microsoft SharePoint 2013 uses ms-publisher URIs as links to Publisher documents stored in SharePoint document libraries.</span></span>
  
### <a name="g-6-interoperability-considerations"></a><span data-ttu-id="66e4e-p181">G-6. Considerações sobre interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="66e4e-p181">G-6. Interoperability Considerations</span></span>

<span data-ttu-id="66e4e-416">Observe que a barra vertical usada como um delimitador nesta especificação não está entre esses caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores.</span><span class="sxs-lookup"><span data-stu-id="66e4e-416">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters.</span></span> <span data-ttu-id="66e4e-417">Isso é feito intencionalmente, para maximizar o conjunto de caracteres que podem ter suporte do argumento do comando URI sem a necessidade de codificar esses caracteres como o símbolo de porcentagem.</span><span class="sxs-lookup"><span data-stu-id="66e4e-417">This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span> <span data-ttu-id="66e4e-418">Em \<command-argument\> segmentos, os caracteres reservados da RFC 3986 ":" e "/" fazem parte dos dados do argumento, não dos delimitadores e, portanto, são incluídos sem proteção.</span><span class="sxs-lookup"><span data-stu-id="66e4e-418">Within \<command-argument\> segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span>
  
### <a name="g-7-security-considerations"></a><span data-ttu-id="66e4e-p183">G-7. Considerações sobre segurança</span><span class="sxs-lookup"><span data-stu-id="66e4e-p183">G-7. Security Considerations</span></span>

<span data-ttu-id="66e4e-p184">Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-publisher, clicar em um link para uma URI ms-publisher fará com que o aplicativo registrado seja iniciado, com instruções para o aplicativo tentar abrir um documento na URI especificada. Os aplicativos que estejam se registrando para processar URIs ms-publisher devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p184">On systems that have registered handlers to recognize and act on ms-publisher URIs, clicking on a link to an ms-publisher URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-publisher URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="g-9-references"></a><span data-ttu-id="66e4e-p185">G-9. Referências</span><span class="sxs-lookup"><span data-stu-id="66e4e-p185">G-9. References</span></span>

<span data-ttu-id="66e4e-425">RFC 3987 \endash identificadores de recurso internacional (íris)</span><span class="sxs-lookup"><span data-stu-id="66e4e-425">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-h---uri-scheme-registration-template-for-ms-spd-scheme"></a><span data-ttu-id="66e4e-426">APÊNDICE H - MODELO DE REGISTRO DE ESQUEMA URI PARA O ESQUEMA MS-SPD</span><span class="sxs-lookup"><span data-stu-id="66e4e-426">APPENDIX H - URI SCHEME REGISTRATION TEMPLATE FOR MS-SPD SCHEME</span></span>
<span data-ttu-id="66e4e-427"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="66e4e-427"><a name="bk_addresources"> </a></span></span>

### <a name="h-3-uri-scheme-syntax"></a><span data-ttu-id="66e4e-p186">H-3. Sintaxe do Esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p186">H-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="66e4e-430">Esquema do SharePoint Designer = "ms-spd:" open-for-edit-cmd</span><span class="sxs-lookup"><span data-stu-id="66e4e-430">SharePoint Designer Scheme = "ms-spd:" open-for-edit-cmd</span></span>
    
> <span data-ttu-id="66e4e-431">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="66e4e-431">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="66e4e-432">document-uri = localização da URI de documento a ser aberto</span><span class="sxs-lookup"><span data-stu-id="66e4e-432">document-uri = URI location of document to open</span></span>
    
### <a name="h-4-uri-scheme-semantics"></a><span data-ttu-id="66e4e-p187">H-4. Semântica do Esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p187">H-4. URI Scheme Semantics</span></span>

<span data-ttu-id="66e4e-p188">O esquema ms-spd define uma sintaxe de URI para abertura ou criação de um documento do Microsoft SharePoint Designer. O esquema define dois comandos que servem como instruções sobre o que deve ser feito com o documento referenciado. Os comandos são 1) open-for-edit-cmd (ofe), que instrui o SharePoint Designer a abrir o documento na URI especificada para edição; 2) open-for-view-cmd (ofv), que instrui o SharePoint Designer a abrir o documento na URI especificada em um modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p188">The ms-spd scheme defines a URI syntax for opening a Microsoft SharePoint Designer document. The scheme defines two commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs SharePoint Designer to open the document at the specified URI for editing; and 2) open-for-view-cmd (ofv), which instructs SharePoint Designer to open the document at the specified URI in a read-only mode.</span></span>
  
### <a name="h-5-applicationsprotocols-that-use-the-ms-spd-uri-scheme"></a><span data-ttu-id="66e4e-p189">H-5. Aplicativos/protocolos que usam o Esquema URI ms-spd</span><span class="sxs-lookup"><span data-stu-id="66e4e-p189">H-5. Applications/Protocols that use the ms-spd URI Scheme</span></span>

<span data-ttu-id="66e4e-p190">O Esquema URI ms-spd é usado pelo Microsoft Office 2013 para invocar o Microsoft SharePoint Designer 2013 de páginas da Web. O Microsoft SharePoint 2013 usa URIs ms-spd como links para documentos do SharePoint Designer armazenados em bibliotecas de documentos do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p190">The ms-spd URI Scheme is used by Microsoft Office 2013 to invoke Microsoft SharePoint Designer 2013 from web pages. Microsoft SharePoint 2013 uses ms-spd URIs as links to SharePoint Designer documents stored in SharePoint document libraries.</span></span>
  
### <a name="h-6-interoperability-considerations"></a><span data-ttu-id="66e4e-p191">H-6. Considerações sobre interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="66e4e-p191">H-6. Interoperability Considerations</span></span>

<span data-ttu-id="66e4e-p192">Observe que a barra vertical usada como um delimitador nesta especificação não está entre esses caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente, para maximizar o conjunto de caracteres que podem ter suporte do argumento do comando URI sem a necessidade de codificar esses caracteres como o símbolo de porcentagem.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p192">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="66e4e-446">Em segmentos < *command-argument*  >, os caracteres reservados da RFC 3986 ":" e "/" fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape.</span><span class="sxs-lookup"><span data-stu-id="66e4e-446">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="h-7-security-considerations"></a><span data-ttu-id="66e4e-p193">H-7. Considerações sobre segurança</span><span class="sxs-lookup"><span data-stu-id="66e4e-p193">H-7. Security Considerations</span></span>

<span data-ttu-id="66e4e-p194">Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-spd, clicar em um link para uma URI ms-spd fará com que o aplicativo registrado seja iniciado, com instruções para o aplicativo tentar abrir um documento na URI especificada. Os aplicativos que estejam se registrando para processar URIs ms-spd devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p194">On systems that have registered handlers to recognize and act on ms-spd URIs, clicking on a link to an ms-spd URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-spd URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="h-8-references"></a><span data-ttu-id="66e4e-p195">H-8. Referências</span><span class="sxs-lookup"><span data-stu-id="66e4e-p195">H-8. References</span></span>

<span data-ttu-id="66e4e-453">RFC 3987 \endash identificadores de recurso internacional (íris)</span><span class="sxs-lookup"><span data-stu-id="66e4e-453">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-i---uri-scheme-registration-template-for-ms-infopath-scheme"></a><span data-ttu-id="66e4e-454">APÊNDICE I - MODELO DE REGISTRO DE ESQUEMA URI PARA O ESQUEMA MS-INFOPATH</span><span class="sxs-lookup"><span data-stu-id="66e4e-454">APPENDIX I - URI SCHEME REGISTRATION TEMPLATE FOR MS-INFOPATH SCHEME</span></span>
<span data-ttu-id="66e4e-455"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="66e4e-455"><a name="bk_addresources"> </a></span></span>

###   <a name="i-3-uri-scheme-syntax"></a><span data-ttu-id="66e4e-p196">I-3. Sintaxe do Esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p196">I-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="66e4e-458">Esquema do Infopath = "ms-infopath:" open-for-edit-cmd | open-for-view-cmd</span><span class="sxs-lookup"><span data-stu-id="66e4e-458">Infopath Scheme = "ms-infopath:" open-for-edit-cmd | open-for-view-cmd</span></span>
    
> <span data-ttu-id="66e4e-459">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="66e4e-459">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="66e4e-460">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="66e4e-460">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="66e4e-461">document-uri = localização da URI de documento a ser aberto</span><span class="sxs-lookup"><span data-stu-id="66e4e-461">document-uri = URI location of document to open</span></span>
    
### <a name="i-4-uri-scheme-semantics"></a><span data-ttu-id="66e4e-p197">I-4. Semântica do Esquema URI</span><span class="sxs-lookup"><span data-stu-id="66e4e-p197">I-4. URI Scheme Semantics</span></span>

<span data-ttu-id="66e4e-464">O esquema ms-infopath define uma sintaxe de URI para abertura ou criação de um documento do Microsoft Infopath.</span><span class="sxs-lookup"><span data-stu-id="66e4e-464">The ms-infopath scheme defines a URI syntax for opening or creating a Microsoft Infopath document.</span></span> <span data-ttu-id="66e4e-465">O esquema define dois comandos que servem como instruções sobre o que deve ser feito com o documento referenciado.</span><span class="sxs-lookup"><span data-stu-id="66e4e-465">The scheme defines two commands that serve as instructions regarding what should be done with the referenced document.</span></span> <span data-ttu-id="66e4e-466">Os comandos são 1) open-for-edit-cmd (ofe), que instrui o InfoPath a abrir o documento na URI especificada para edição; e 2) open-for-view-cmd (ofv), que instrui o InfoPath a abrir o documento no URI especificado em um modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="66e4e-466">The commands are 1) open-for-edit-cmd (ofe), which instructs InfoPath to open the document at the specified URI for editing; and 2) open-for-view-cmd (ofv), which instructs InfoPath to open the document at the specified URI in a read-only mode.</span></span>
  
### <a name="i-5-applicationsprotocols-that-use-the-ms-infopath-uri-scheme"></a><span data-ttu-id="66e4e-p199">I-5. Aplicativos/protocolos que usam o Esquema URI ms-infopath</span><span class="sxs-lookup"><span data-stu-id="66e4e-p199">I-5. Applications/Protocols that use the ms-infopath URI Scheme</span></span>

<span data-ttu-id="66e4e-p200">O Esquema URI ms-infopath é usado pelo Microsoft Office 2013 para invocar o Microsoft Infopath 2013 de páginas da Web. O Microsoft SharePoint 2013 usa URIs ms-infopath como links para documentos do Infopath armazenados em bibliotecas de documentos do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p200">The ms-infopath URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Infopath 2013 from web pages. Microsoft SharePoint 2013 uses ms-infopath URIs as links to Infopath documents stored in SharePoint document libraries.</span></span>
  
### <a name="i-6-interoperability-considerations"></a><span data-ttu-id="66e4e-p201">I-6. Considerações sobre interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="66e4e-p201">I-6. Interoperability Considerations</span></span>

<span data-ttu-id="66e4e-p202">Observe que a barra vertical usada como um delimitador nesta especificação não está entre esses caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente, para maximizar o conjunto de caracteres que podem ter suporte do argumento do comando URI sem a necessidade de codificar esses caracteres como o símbolo de porcentagem.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p202">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="66e4e-475">Em segmentos < *command-argument*  >, os caracteres reservados da RFC 3986 ":" e "/" fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape.</span><span class="sxs-lookup"><span data-stu-id="66e4e-475">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="i-7-security-considerations"></a><span data-ttu-id="66e4e-p203">I-7. Considerações sobre segurança</span><span class="sxs-lookup"><span data-stu-id="66e4e-p203">I-7. Security Considerations</span></span>

<span data-ttu-id="66e4e-p204">Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-infopath, clicar em um link para uma URI ms-infopath fará com que o aplicativo registrado seja iniciado, com instruções para o aplicativo tentar abrir um documento na URI especificada. Os aplicativos que estejam se registrando para processar URIs ms-infopath devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="66e4e-p204">On systems that have registered handlers to recognize and act on ms-infopath URIs, clicking on a link to an ms-infopath URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-infopath URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="i-8-references"></a><span data-ttu-id="66e4e-p205">I-8. Referências</span><span class="sxs-lookup"><span data-stu-id="66e4e-p205">I-8. References</span></span>

<span data-ttu-id="66e4e-482">RFC 3987 \endash identificadores de recurso internacional (íris)</span><span class="sxs-lookup"><span data-stu-id="66e4e-482">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
