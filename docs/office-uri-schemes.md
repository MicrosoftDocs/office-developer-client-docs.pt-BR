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
# <a name="office-uri-schemes"></a>Esquemas de URI do Office

## <a name="11-abstract"></a>1.1 RESUMO

Este documento define o formato de URIs (Uniform Resource Identifiers) para aplicativos de produtividade do escritório. O esquema tem suporte no Microsoft Office 2010 Service Pack 2 e posterior, incluindo o Microsoft Office 2013 para Windows e os produtos do Microsoft SharePoint 2013. Também tem suporte no Office for iPhone, Office for iPad e no Office for Mac 2011.
  
## <a name="12-introduction"></a>1.2 INTRODUÇÃO

Estes esquemas de URI permitem que aplicativos de produtividade de escritório sejam chamados com vários comandos. Cada aplicativo recebe um esquema nomeado diferente, mas todos os esquemas seguem as mesmas regras para como a URI é formada (Esquema de URI).
  
## <a name="13-uri-schema"></a>1.3 ESQUEMA DE URI

### <a name="full-schema"></a>Esquema completo

< *scheme-name*  >:<  *command-name*  >"|"<  *command-argument-descriptor*  > "|"<  *command-argument*  > 
  
Uma URI como definida neste documento pode ter um ou mais argumentos de comando, cada um deve incluir os elementos < *descritor-command-argument*  > e <  *command-argument*  > e ser delimitada pelo caractere de barra vertical ("|"). Quando mais de um argumento de comando for incluído em uma URI, deverá haver um caractere de barra vertical ("|") separando cada argumento de comando do argumento de comando a seguir. 
  
Esses esquemas não incluem um componente de autoridade como definido na seção 3.2 da RFC 3986. A invocação dos comandos especificados neste documento ocorre no contexto do sistema que está invocando o comando. Por exemplo, quando a URI "ms-excel:ofv|u|https://contoso/Q4/budget.xls" for invocada de um computador pessoal que esteja executando o Microsoft Windows com o Microsoft Office 2013 instalado, o resultado esperado é a instalação local do Microsoft Excel ser iniciada e os argumentos passados para abrir o arquivo em  *https://contoso/Q4/budget.xls*  em modo somente leitura. Observe que a barra vertical usada como um delimitador nesta especificação não está entre os caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente para maximizar o conjunto de caracteres com suporte do argumento do comando de URI sem a necessidade de codificar esses caracteres codificados por porcentagem. 
  
A sintaxe do esquema inclui o seguinte:
  
1. < *scheme-name*  >: Isso se refere ao tipo de aplicativo que deve ser invocado. Por exemplo, o nome de esquema ms-word: está registrado pelo Microsoft Word. 
    
2. Separador ":"
    
3. < *command-name*  >: descreve as ações que o aplicativo deve executar. Por exemplo, a abertura de um documento para exibição. A lista de nomes de comando é descrita na seção 1.5. 
    
4. Separador "|" (barra vertical)
    
5. < *command-argument-descriptor*  >: esse elemento oferece mais informações sobre o que argumento de comando trata. 
    
6. Separador "|" (barra vertical)
    
7. < *command-argument*  >: os argumentos variam dependendo do comando. Um argumento comum é a URI para um documento tipicamente usando o esquema http ou https. Observe que, em segmentos <  *command-argument*  >, os caracteres reservados ":" e "/" da RFC 3986 fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape. 
    
### <a name="abbreviated-schema"></a>Esquema abreviado

Uma forma abreviada dos esquemas URI de escritório permite uma solicitação mais compacta para iniciar um aplicativo do Office especificado para abrir o recurso localizado em uma determinada URI. Essa forma abreviada implica no < *command-name*  > "ofv" e no <  *descritor-command-argument*  > "u". Nenhum outro controle ou argumentos de comando são permitidos neste esquema. 
  
< *scheme-name*  >:<  *command-argument*  > 
  
1. < *scheme-name*  >: o tipo de aplicativo que deve ser invocado. Por exemplo, ms-word: para Microsoft Word. 
    
2. < *command-argument*  >: URI para o recurso que o aplicativo deve abrir. Atualmente, somente URIs baseadas no esquema http ou https têm suporte. 
    
## <a name="14-scheme-names-and-office-application-registrations"></a>1.4 NOMES DE ESQUEMA E REGISTROS DE APLICATIVO DO OFFICE

A seguir, a lista de nomes de esquema implementados nos aplicativos do Microsoft Office. Quando o Microsoft Office estiver instalado, cada nome de esquema será registrado no Windows para ser manipulado pelo produto do Office do mesmo nome. Observe que "ms-spd" é uma abreviação de SharePoint Designer.
  
> - *ms-word:* 
    
> - *ms-powerpoint:* 
    
> - *ms-excel:* 
    
> - *ms-visio:* 
    
> - *ms-access:* 
    
> - *ms-project:* 
    
> - *ms-publisher:* 
    
> - *ms-spd:* 
    
> - *ms-infopath:* 
    
## <a name="15-commands-and-required-command-arguments"></a>1.5 COMANDOS E ARGUMENTOS DE COMANDO NECESSÁRIOS

### <a name="view-document"></a>Exibir Documento

O comando a seguir fará com que o aplicativo abra o documento referenciado pela URI em um modo somente leitura ou de exibição.
  
> Nome do comando: ofv
    
> Descritor de argumento de comando: u
    
> Argumento de comando: uma URI para o documento, com base no esquema http ou https
    
> Exemplo:  *ms-excel:ofv|u|https://contoso/Q4/budget.xls* 
    
### <a name="edit-document"></a>Editar Documento

O comando a seguir fará com que o aplicativo abra o documento referenciado pela URI em modo de edição.
  
> Nome do comando: ofe
    
> Descritor de argumento de comando: u
    
> Argumento de comando: uma URI para o documento, com base no esquema http ou https
    
> Exemplo:  *ms-powerpoint:ofe|u|https://www.fourthcoffee.com/AllHandsDeck.ppt* 
    
### <a name="new-document-from-template"></a>Novo Documento do Modelo

O comando a seguir fará com que o aplicativo crie e abra um novo documento com base no modelo armazenado na URI especificada. O arquivo de modelo não é modificado nesse processo. Um argumento de comando adicional pode ser fornecido para especificar o caminho padrão oferecido como um local de salvamento quando o arquivo for salvo pela primeira vez. O usuário pode escolher uma localização diferente.
  
> Nome do comando: nft
    
> Descritor de argumento de comando 1: u
    
> Argumento de comando 1: uma URI para o modelo, com base no esquema http ou https
    
> Descritor de argumento de comando opcional 2: s
    
> Argumento de comando opcional 2: URI para especificar a pasta de salvamento padrão
    
> Exemplo:  *ms-word:nft|u|https://cohowinery/templates/elegance.pot|s|https://cohowinery/presentations* 
    
Como uma observação, se a localização de salvamento padrão opcional for fornecida, deve estar apontando para o mesmo nome de host como o modelo.
  
Adicionalmente, os aplicativos SharePoint Designer e InfoPath (que implementa os esquemas ms-spd: e ms-infopath:, respectivamente) não dão suporte à funcionalidade "novo documento do modelo".
  
## <a name="16-backwards-compatibility"></a>1.6 COMPATIBILIDADE COM VERSÕES ANTERIORES

Ao analisar uma URI para extrair os argumentos de comando apropriados para um determinado comando, o manipulador de URI do Office só usará os argumentos de comando com o descritor de argumento de comando esperado. Se houver pares de argumentos e descritores de argumento adicionais com descritores de argumento inesperados, eles serão removidos da URI. Esse mecanismo permite que versões futuras do esquema adicionem argumentos de comando adicionais sem interromper a compatibilidade com versões anteriores com implementações legadas desse esquema.
  
## <a name="17-implementation-restrictions-on-command-arguments"></a>1.7 RESTRIÇÕES DE IMPLEMENTAÇÃO SOBRE ARGUMENTOS DE COMANDO

As restrições abaixo são posicionadas em argumentos de comando em sua implementação atual no Office 2013.
  
### <a name="length-limitations-on-uri-command-arguments"></a>Limitações de tamanho em argumentos de comando de URI

Para argumentos de comando de URI, o tamanho máximo de caminho é de 256 caracteres para todos os aplicativos, exceto o Excel, onde o limite é 216. Tamanhos de caminho maiores do que esse podem ter suporte aplicativo por aplicativo e recomenda-se testar antes de implantar todas as soluções que utilizam isso.
  
### <a name="allowed-characters-in-uri-command-arguments"></a>Caracteres permitidos em argumentos de comando de URI

Os URIs permitidos devem estar em conformidade com os padrões propostos em RFC 3987-internacionalizated Resource Identifiers (íris). Os caracteres identificados como reservados na RFC 3986 não devem ser codificados por porcentagem. . Os nomes de FileNames não devem conter nenhum dos seguintes caracteres: \/:? \< \> | "ou \* .  
  
## <a name="appendix-a---uri-scheme-registration-template-for-ms-word-scheme"></a>APÊNDICE A - MODELO DE REGISTRO DE ESQUEMA URI PARA O ESQUEMA MS-WORD
<a name="bk_addresources"> </a>

### <a name="a-3-uri-scheme-syntax"></a>A-3. Sintaxe do esquema URI

> Esquema do Word = "ms-word:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = localização da URI de documento a ser aberto
    
> template-uri = localização da URI de arquivo de modelo em que o novo arquivo se baseará
    
> save-location = localização da URI da pasta em que o novo documento deve ser criado
    
### <a name="a-4-uri-scheme-semantics"></a>A-4. Semântica do esquema URI

O esquema ms-word define uma sintaxe de URI para abertura ou criação de um documento de processamento de texto. O esquema define três comandos que servem como instruções sobre o que deve ser feito com o documento referenciado. Os comandos são 1) open-for-edit-cmd (ofe), que instrui um aplicativo de processamento de texto a abrir o documento na URI especificada para edição; 2) open-for-view-cmd (ofv), que instrui um aplicativo de processamento de texto a abrir o documento na URI especificada em um modo somente leitura e 3) new-from-template-cmd (nft), que instrui um aplicativo de processamento de texto para criar um novo documento com base no modelo de documento localizado na URI template-uri especificada e salvar o novo documento na localização especificada na URI save-location opcional ou, na ausência dessa URI opcional, na localização da biblioteca de documentos padrão.
  
### <a name="a-5-applicationsprotocols-that-use-the-ms-word-uri-scheme"></a>A-5. Aplicativos/protocolos que usam o Esquema URI ms-word

O Esquema URI ms-word URI é usado pelo Microsoft Office 2013 para invocar o Microsoft Word 2013 ou o Microsoft Word 2010 com Service Pack 2. O Microsoft SharePoint 2013 usa URIs ms-word como links para documentos de processamento de texto armazenados em bibliotecas de documentos do SharePoint.
  
### <a name="a-6-interoperability-considerations"></a>A-6. Considerações sobre interoperabilidade

Observe que a barra vertical usada como um delimitador nesta especificação não está entre os caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente para maximizar o conjunto de caracteres com suporte do argumento do comando de URI sem a necessidade de codificar esses caracteres codificados por porcentagem.
  
Em segmentos < *command-argument*  >, os caracteres reservados da RFC 3986 ":" e "/" fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape. 
  
### <a name="a-7-security-considerations"></a>A-7. Considerações sobre segurança

 Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-word, clicar em um link para uma URI ms-word fará com que o aplicativo de processamento de texto registrado seja iniciado, com instruções para o aplicativo de processamento de texto tentar abrir um documento na URI especificada. Os aplicativos de processamento de texto que estejam se registrando para processar URIs ms-word devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado. 
  
### <a name="a-8-references"></a>A-8. Referências

RFC 3987 \endash identificadores de recurso internacional (íris)  
  
## <a name="appendix-b---uri-scheme-registration-template-for-ms-powerpoint-scheme"></a>APÊNDICE B - MODELO DE REGISTRO DE ESQUEMA URI PARA O ESQUEMA MS-POWERPOINT
<a name="bk_addresources"> </a>

### <a name="b-3-uri-scheme-syntax"></a>B-3. Sintaxe do Esquema URI

- Esquema do PowerPoint = "ms-powerpoint:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
- open-for-edit-cmd = "ofe|u|" document-uri
    
- open-for-view-cmd = "ofv|u|" document-uri
    
- new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
- document-uri = localização da URI de documento a ser aberto
    
- template-uri = localização da URI de arquivo de modelo em que o novo arquivo se baseará
    
- save-location\* = localização da URI de pasta na qual o novo documento deve ser criado
    
- \*save-location é um parâmetro opcional
    
### <a name="b-4-uri-scheme-semantics"></a>B-4. Semântica do Esquema URI

O esquema ms-powerpoint define uma sintaxe de URI para abertura ou criação de um documento de apresentação. O esquema define três comandos que servem como instruções sobre o que deve ser feito com o documento referenciado. Os comandos são 1) open-for-edit-cmd (ofe), que instrui um aplicativo de apresentação a abrir o documento na URI especificada para edição; 2) open-for-view-cmd (ofv), que instrui um aplicativo de apresentação a abrir o documento na URI especificada em um modo somente leitura e 3) new-from-template-cmd (nft), que instrui um aplicativo de apresentação para criar um novo documento com base no modelo de documento localizado na URI template-uri especificado e salvar o novo documento na localização especificada na URI save-location opcional ou, na ausência dessa URI opcional, na localização da biblioteca de documentos padrão.
  
### <a name="b-5-applicationsprotocols-that-use-the-ms-powerpoint-uri-scheme"></a>B-5. Aplicativos/protocolos que usam o Esquema URI ms-powerpoint

O Esquema URI ms-powerpoint é usado pelo Microsoft Office 2013 para invocar o Microsoft PowerPoint 2013 ou o Microsoft PowerPoint 2010 com Service Pack 2. O Microsoft SharePoint 2013 usa URIs ms-powerpoint como links para documentos de apresentação armazenados em bibliotecas de documentos do SharePoint.
  
### <a name="b-6-interoperability-considerations"></a>B-6. Considerações sobre interoperabilidade

Observe que a barra vertical usada como um delimitador nesta especificação não está entre esses caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente, para maximizar o conjunto de caracteres que podem ter suporte do argumento do comando URI sem a necessidade de codificar esses caracteres como o símbolo de porcentagem.
  
Em segmentos < *command-argument*  >, os caracteres reservados da RFC 3986 ":" e "/" fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape. 
  
### <a name="b-7-security-considerations"></a>B-7. Considerações sobre segurança

Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-powerpoint, clicar em um link para uma URI ms-powerpoint fará com que o aplicativo de apresentação registrado seja iniciado, com instruções para o aplicativo de apresentação tentar abrir um documento na URI especificada. Os aplicativos de apresentação que estejam se registrando para processar URIs ms-powerpoint devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado.
  
### <a name="b-8-references"></a>B-8. Referências

RFC 3987 \endash identificadores de recurso internacional (íris)  
  
## <a name="appendix-c---uri-scheme-registration-template-for-ms-excel-scheme"></a>APÊNDICE C - MODELO DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-EXCEL
<a name="bk_addresources"> </a>

### <a name="c-3-uri-scheme-syntax"></a>C-3. Sintaxe do Esquema URI

> Esquema do Excel = "ms-excel:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = localização da URI de documento a ser aberto
    
> template-uri = localização da URI de arquivo de modelo em que o novo arquivo se baseará
    
> save-location\* = localização da URI de pasta na qual o novo documento deve ser criado
    
> \*save-location é um parâmetro opcional
    
### <a name="c-4-uri-scheme-semantics"></a>C-4. Semântica do Esquema URI

O esquema ms-excel define uma sintaxe de URI para abertura ou criação de um documento de planilha. O esquema define três comandos que servem como instruções sobre o que deve ser feito com o documento referenciado. Os comandos são 1) open-for-edit-cmd (ofe), que instrui um aplicativo de planilha a abrir o documento na URI especificada para edição; 2) open-for-view-cmd (ofv), que instrui um aplicativo de planilha a abrir o documento na URI especificada em um modo somente leitura e 3) new-from-template-cmd (nft), que instrui um aplicativo de planilha para criar um novo documento com base no modelo de documento localizado na URI template-uri especificada e salvar o novo documento na localização especificada na URI save-location opcional ou, na ausência dessa URI opcional, na localização da biblioteca de documentos padrão.
  
### <a name="c-5-applicationsprotocols-that-use-the-ms-excel-uri-scheme"></a>C-5. Aplicativos/protocolos que usam o Esquema URI ms-excel

O Esquema URI ms-excel é usado pelo Microsoft Office 2013 para invocar o Microsoft Excel 2013 ou o Microsoft Excel 2010 com Service Pack 2. O Microsoft SharePoint 2013 usa URIs ms-excel como links para documentos de planilha armazenados em bibliotecas de documentos do SharePoint.
  
### <a name="c-6-interoperability-considerations"></a>C-6. Considerações sobre interoperabilidade

Observe que a barra vertical usada como um delimitador nesta especificação não está entre esses caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente, para maximizar o conjunto de caracteres que podem ter suporte do argumento do comando URI sem a necessidade de codificar esses caracteres como o símbolo de porcentagem.
  
Em segmentos < *command-argument*  >, os caracteres reservados da RFC 3986 ":" e "/" fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape. 
  
### <a name="c-7-security-considerations"></a>C-7. Considerações sobre segurança

Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-excel, clicar em um link para uma URI ms-excel fará com que o aplicativo de planilha registrado seja iniciado, com instruções para o aplicativo tentar abrir um documento na URI especificada. Os aplicativos que estejam se registrando para processar URIs ms-excel devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado.
  
### <a name="c-8-references"></a>C-8. Referências

RFC 3987 \endash identificadores de recurso internacional (íris)  
  
## <a name="appendix-d---uri-scheme-registration-template-for-ms-visio-scheme"></a>APÊNDICE D - MODELO DE REGISTRO DE ESQUEMA URI PARA O ESQUEMA MS-VISIO
<a name="bk_addresources"> </a>

### <a name="d-3-uri-scheme-syntax"></a>D-3. Sintaxe do Esquema URI

> Esquema do Visio = "ms-visio:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = localização da URI de documento a ser aberto
    
> template-uri = localização da URI de arquivo de modelo em que o novo arquivo se baseará
    
> save-location\* = localização da URI de pasta na qual o novo documento deve ser criado
    
> \*save-location é um parâmetro opcional
    
### <a name="d-4-uri-scheme-semantics"></a>D-4. Semântica do Esquema URI

O esquema ms-visio define uma sintaxe de URI para abertura ou criação de um documento do Microsoft Visio. O esquema define três comandos que servem como instruções sobre o que deve ser feito com o documento referenciado. Os comandos são 1) open-for-edit-cmd (ofe), que instrui o Visio a abrir o documento na URI especificada para edição; 2) open-for-view-cmd (ofv), que instrui o Visio a abrir o documento na URI especificada em um modo somente leitura e 3) new-from-template-cmd (nft), que instrui o Visio a criar um novo documento com base no modelo de documento localizado na URI template-uri especificado e salvar o novo documento na localização especificada na URI save-location opcional ou, na ausência dessa URI opcional, na localização da biblioteca de documentos padrão.
  
### <a name="d-5-applicationsprotocols-that-use-the-ms-visio-uri-scheme"></a>D-5. Aplicativos/protocolos que usam o Esquema URI ms-visio

O Esquema URI ms-visio é usado pelo Microsoft Office 2013 para invocar o Microsoft Visio 2013 ou o Microsoft Visio 2010 com Service Pack 2. O Microsoft SharePoint 2013 usa URIs ms-visio como links para documentos do Visio armazenados em bibliotecas de documentos do SharePoint.
  
### <a name="d-6-interoperability-considerations"></a>D-6. Considerações sobre interoperabilidade

Observe que a barra vertical usada como um delimitador nesta especificação não está entre esses caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente, para maximizar o conjunto de caracteres que podem ter suporte do argumento do comando URI sem a necessidade de codificar esses caracteres como o símbolo de porcentagem.
  
Em segmentos < *command-argument*  >, os caracteres reservados da RFC 3986 ":" e "/" fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape. 
  
### <a name="d-7-security-considerations"></a>D-7. Considerações sobre segurança

Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-visio, clicar em um link para uma URI ms-visio fará com que o aplicativo registrado seja iniciado, com instruções para o aplicativo tentar abrir um documento na URI especificada. Os aplicativos que estejam se registrando para processar URIs ms-visio devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado.
  
### <a name="d-8-references"></a>D-8. Referências

RFC 3987 \endash identificadores de recurso internacional (íris)
  
## <a name="appendix-e---uri-scheme-registration-template-for-ms-access-scheme"></a>APÊNDICE E - MODELO DE REGISTRO DE ESQUEMA URI PARA O ESQUEMA MS-ACCESS
<a name="bk_addresources"> </a>

### <a name="e-3-uri-scheme-syntax"></a>E-3. Sintaxe do Esquema URI

> Esquema do Access = "ms-access:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = localização da URI de documento a ser aberto
    
> template-uri = localização da URI de arquivo de modelo em que o novo arquivo se baseará
    
> save-location\* = localização da URI de pasta na qual o novo documento deve ser criado
    
> \*save-location é um parâmetro opcional
    
### <a name="e-4-uri-scheme-semantics"></a>E-4. Semântica do Esquema URI

O esquema ms-access define uma sintaxe de URI para abertura ou criação de um banco de dados. O esquema define três comandos que servem como instruções sobre o que deve ser feito com o arquivo de banco de dados referenciado. Os comandos são 1) open-for-edit-cmd (ofe), que instrui o aplicativo de banco de dados a abrir o documento na URI especificada para edição; 2) open-for-view-cmd (ofv), que instrui o aplicativo de banco de dados a abrir o documento na URI especificada em um modo somente leitura e 3) new-from-template-cmd (nft), que instrui o aplicativo de banco de dados a criar um novo documento com base no modelo de documento localizado na URI template-uri especificado e salvar o novo banco de dados na localização especificada na URI save-location opcional ou, na ausência dessa URI opcional, na localização da biblioteca de documentos padrão.
  
### <a name="e-5-applicationsprotocols-that-use-the-ms-access-uri-scheme"></a>E-5. Aplicativos/protocolos que usam o Esquema URI ms-access

O Esquema URI ms-access é usado pelo Microsoft Office 2013 para invocar o Microsoft Access 2013 ou o Microsoft Access 2010 com Service Pack 2 de páginas da Web. O Microsoft SharePoint 2013 usa URIs ms-access como links para bancos de dados do Access armazenados em bibliotecas de documentos do SharePoint.
  
### <a name="e-6-interoperability-considerations"></a>E-6. Considerações sobre interoperabilidade

Observe que a barra vertical usada como um delimitador nesta especificação não está entre esses caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente, para maximizar o conjunto de caracteres que podem ter suporte do argumento do comando URI sem a necessidade de codificar esses caracteres como o símbolo de porcentagem. Em \<command-argument\> segmentos, os caracteres reservados RFC 3986 ":" e "/" fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape.
  
### <a name="e-7-security-considerations"></a>E-7. Considerações sobre segurança

Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-access, clicar em um link para uma URI ms-access fará com que o aplicativo registrado seja iniciado, com instruções para o aplicativo tentar abrir um banco de dados na URI especificada. Os aplicativos que estejam se registrando para processar URIs ms-access devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado.
  
### <a name="e-8-references"></a>E-8. Referências

RFC 3987 \endash identificadores de recurso internacional (íris)  
  
## <a name="appendix-f---uri-scheme-registration-template-for-ms-project-scheme"></a>APÊNDICE F - MODELO DE REGISTRO DE ESQUEMA URI PARA O ESQUEMA MS-PROJECT
<a name="bk_addresources"> </a>

### <a name="f-3-uri-scheme-syntax"></a>F-3. Sintaxe do Esquema URI

> Esquema do Project = "ms-project:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = localização da URI de documento a ser aberto
    
> template-uri = localização da URI de arquivo de modelo em que o novo arquivo se baseará
    
> save-location\* = localização da URI de pasta na qual o novo documento deve ser criado
    
> \*save-location é um parâmetro opcional
    
### <a name="f-4-uri-scheme-semantics"></a>F-4. Semântica do Esquema URI

O esquema ms-project define uma sintaxe de URI para abertura ou criação de um documento do Microsoft Project. O esquema define três comandos que servem como instruções sobre o que deve ser feito com o documento referenciado. Os comandos são 1) open-for-edit-cmd (ofe), que instrui o Project a abrir o documento na URI especificada para edição; 2) open-for-view-cmd (ofv), que instrui o Project a abrir o documento na URI especificada em um modo somente leitura e 3) new-from-template-cmd (nft), que instrui o Project para criar um novo documento com base no modelo de documento localizado na URI template-uri especificado e salvar o novo documento na localização especificada na URI save-location opcional ou, na ausência dessa URI opcional, na localização da biblioteca de documentos padrão.
  
### <a name="f-5-applicationsprotocols-that-use-the-ms-project-uri-scheme"></a>F-5. Aplicativos/protocolos que usam o Esquema URI ms-project

O Esquema URI ms-project é usado pelo Microsoft Office 2013 para invocar o Microsoft Project 2013 de páginas da Web. O Microsoft SharePoint 2013 usa URIs ms-project como links para documentos do Project armazenados em bibliotecas de documentos do SharePoint.
  
### <a name="f-6-interoperability-considerations"></a>F-6. Considerações sobre interoperabilidade

Observe que a barra vertical usada como um delimitador nesta especificação não está entre esses caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente, para maximizar o conjunto de caracteres que podem ter suporte do argumento do comando URI sem a necessidade de codificar esses caracteres como o símbolo de porcentagem.
  
Em segmentos < *command-argument*  >, os caracteres reservados da RFC 3986 ":" e "/" fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape. 
  
### <a name="f-7-security-considerations"></a>F-7. Considerações sobre segurança

Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-project, clicar em um link para uma URI ms-project fará com que o aplicativo registrado seja iniciado, com instruções para o aplicativo tentar abrir um documento na URI especificada. Os aplicativos que estejam se registrando para processar URIs ms-project devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado.
  
### <a name="f-8-references"></a>F-8. Referências

RFC 3987 \endash identificadores de recurso internacional (íris)  
  
## <a name="appendix-g---uri-scheme-registration-template-for-ms-publisher-scheme"></a>APÊNDICE G - MODELO DE REGISTRO DE ESQUEMA URI PARA O ESQUEMA MS-PUBLISHER
<a name="bk_addresources"> </a>

### <a name="g-3-uri-scheme"></a>G-3. Esquema URI

> Sintaxe Esquema do Publisher = "ms-publisher:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = localização da URI de documento a ser aberto
    
> template-uri = localização da URI de arquivo de modelo em que o novo arquivo se baseará
    
> save-location\* = localização da URI de pasta na qual o novo documento deve ser criado
    
> \*save-location é um parâmetro opcional
    
### <a name="g-4-uri-scheme-semantics"></a>G-4. Semântica do Esquema URI

O esquema ms-publisher define uma sintaxe de URI para abertura ou criação de um documento do Microsoft Publisher. O esquema define três comandos que servem como instruções sobre o que deve ser feito com o documento referenciado. Os comandos são 1) open-for-edit-cmd (ofe), que instrui o Publisher a abrir o documento na URI especificada para edição; 2) open-for-view-cmd (ofv), que instrui o Publisher a abrir o documento na URI especificada em um modo somente leitura e 3) new-from-template-cmd (nft), que instrui o Publisher para criar um novo documento com base no modelo de documento localizado na URI template-uri especificada e salvar o novo documento na localização especificada na URI save-location opcional ou, na ausência dessa URI opcional, na localização da biblioteca de documentos padrão.
  
### <a name="g-5-applicationsprotocols-that-use-the-ms-publisher-uri-scheme"></a>G-5. Aplicativos/protocolos que usam o Esquema URI ms-publisher

O Esquema URI ms-publisher é usado pelo Microsoft Office 2013 para invocar o Microsoft Publisher 2013 ou o Microsoft Publisher 2010 com Service Pack 2 de páginas da Web. O Microsoft SharePoint 2013 usa URIs ms-publisher como links para documentos do Publisher armazenados em bibliotecas de documentos do SharePoint.
  
### <a name="g-6-interoperability-considerations"></a>G-6. Considerações sobre interoperabilidade

Observe que a barra vertical usada como um delimitador nesta especificação não está entre esses caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente, para maximizar o conjunto de caracteres que podem ter suporte do argumento do comando URI sem a necessidade de codificar esses caracteres como o símbolo de porcentagem. Em \<command-argument\> segmentos, os caracteres reservados RFC 3986 ":" e "/" fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape.
  
### <a name="g-7-security-considerations"></a>G-7. Considerações sobre segurança

Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-publisher, clicar em um link para uma URI ms-publisher fará com que o aplicativo registrado seja iniciado, com instruções para o aplicativo tentar abrir um documento na URI especificada. Os aplicativos que estejam se registrando para processar URIs ms-publisher devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado.
  
### <a name="g-9-references"></a>G-9. Referências

RFC 3987 \endash identificadores de recurso internacional (íris)  
  
## <a name="appendix-h---uri-scheme-registration-template-for-ms-spd-scheme"></a>APÊNDICE H - MODELO DE REGISTRO DE ESQUEMA URI PARA O ESQUEMA MS-SPD
<a name="bk_addresources"> </a>

### <a name="h-3-uri-scheme-syntax"></a>H-3. Sintaxe do Esquema URI

> Esquema do SharePoint Designer = "ms-spd:" open-for-edit-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> document-uri = localização da URI de documento a ser aberto
    
### <a name="h-4-uri-scheme-semantics"></a>H-4. Semântica do Esquema URI

O esquema ms-spd define uma sintaxe de URI para abertura ou criação de um documento do Microsoft SharePoint Designer. O esquema define dois comandos que servem como instruções sobre o que deve ser feito com o documento referenciado. Os comandos são 1) open-for-edit-cmd (ofe), que instrui o SharePoint Designer a abrir o documento na URI especificada para edição; 2) open-for-view-cmd (ofv), que instrui o SharePoint Designer a abrir o documento na URI especificada em um modo somente leitura.
  
### <a name="h-5-applicationsprotocols-that-use-the-ms-spd-uri-scheme"></a>H-5. Aplicativos/protocolos que usam o Esquema URI ms-spd

O Esquema URI ms-spd é usado pelo Microsoft Office 2013 para invocar o Microsoft SharePoint Designer 2013 de páginas da Web. O Microsoft SharePoint 2013 usa URIs ms-spd como links para documentos do SharePoint Designer armazenados em bibliotecas de documentos do SharePoint.
  
### <a name="h-6-interoperability-considerations"></a>H-6. Considerações sobre interoperabilidade

Observe que a barra vertical usada como um delimitador nesta especificação não está entre esses caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente, para maximizar o conjunto de caracteres que podem ter suporte do argumento do comando URI sem a necessidade de codificar esses caracteres como o símbolo de porcentagem.
  
Em segmentos < *command-argument*  >, os caracteres reservados da RFC 3986 ":" e "/" fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape. 
  
### <a name="h-7-security-considerations"></a>H-7. Considerações sobre segurança

Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-spd, clicar em um link para uma URI ms-spd fará com que o aplicativo registrado seja iniciado, com instruções para o aplicativo tentar abrir um documento na URI especificada. Os aplicativos que estejam se registrando para processar URIs ms-spd devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado.
  
### <a name="h-8-references"></a>H-8. Referências

RFC 3987 \endash identificadores de recurso internacional (íris)  
  
## <a name="appendix-i---uri-scheme-registration-template-for-ms-infopath-scheme"></a>APÊNDICE I - MODELO DE REGISTRO DE ESQUEMA URI PARA O ESQUEMA MS-INFOPATH
<a name="bk_addresources"> </a>

###   <a name="i-3-uri-scheme-syntax"></a>I-3. Sintaxe do Esquema URI

> Esquema do Infopath = "ms-infopath:" open-for-edit-cmd | open-for-view-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> document-uri = localização da URI de documento a ser aberto
    
### <a name="i-4-uri-scheme-semantics"></a>I-4. Semântica do Esquema URI

O esquema ms-infopath define uma sintaxe de URI para abertura ou criação de um documento do Microsoft Infopath. O esquema define dois comandos que servem como instruções sobre o que deve ser feito com o documento referenciado. Os comandos são 1) Open-for-Edit-cmd (ofe), que instrui o InfoPath a abrir o documento no URI especificado para edição; e 2) Open-for-View-cmd (OFV), que instrui o InfoPath a abrir o documento no URI especificado em um modo somente leitura.
  
### <a name="i-5-applicationsprotocols-that-use-the-ms-infopath-uri-scheme"></a>I-5. Aplicativos/protocolos que usam o Esquema URI ms-infopath

O Esquema URI ms-infopath é usado pelo Microsoft Office 2013 para invocar o Microsoft Infopath 2013 de páginas da Web. O Microsoft SharePoint 2013 usa URIs ms-infopath como links para documentos do Infopath armazenados em bibliotecas de documentos do SharePoint.
  
### <a name="i-6-interoperability-considerations"></a>I-6. Considerações sobre interoperabilidade

Observe que a barra vertical usada como um delimitador nesta especificação não está entre esses caracteres identificados na seção 2.2 da RFC 3986 como reservados para uso potencial como delimitadores. Isso é feito intencionalmente, para maximizar o conjunto de caracteres que podem ter suporte do argumento do comando URI sem a necessidade de codificar esses caracteres como o símbolo de porcentagem.
  
Em segmentos < *command-argument*  >, os caracteres reservados da RFC 3986 ":" e "/" fazem parte dos dados do argumento e não dos delimitadores e, portanto, são incluídos sem escape. 
  
### <a name="i-7-security-considerations"></a>I-7. Considerações sobre segurança

Em sistemas com manipuladores registrados para reconhecer e agir em URIs ms-infopath, clicar em um link para uma URI ms-infopath fará com que o aplicativo registrado seja iniciado, com instruções para o aplicativo tentar abrir um documento na URI especificada. Os aplicativos que estejam se registrando para processar URIs ms-infopath devem implementar proteções para impedir que documentos sejam abertos de sistemas remotos não confiáveis que possam incluir código mal-intencionado.
  
### <a name="i-8-references"></a>I-8. Referências

RFC 3987 \endash identificadores de recurso internacional (íris)  
  
