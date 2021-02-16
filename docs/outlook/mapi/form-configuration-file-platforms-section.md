---
title: Seção Arquivo de Configuração de Formulário [Plataformas]
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7439de5b91cefe89eba2f9395595d4a7c8ca3ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419125"
---
# <a name="form-configuration-file-platforms-section"></a>Seção Arquivo de Configuração de Formulário [Plataformas]

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A **seção [Plataformas]** lista o conjunto completo de plataformas com suporte neste formulário. Cada entrada de plataforma consiste no **prefixo Platform.** _cadeia_ de caracteres ,  _onde cadeia de_ caracteres é um código de cadeia de caracteres arbitrário para a plataforma. Cada cadeia de caracteres corresponde à **entrada da CPU** de uma seção **[Plataformas]** individuais. Cada entrada em uma **seção [Plataformas]** define uma  _cadeia_ de caracteres de plataforma que faz referência a uma **[plataforma] subsequente.** _cadeia de caracteres_ **de plataforma ]** conforme mostrado aqui. 
  
A **seção [Plataformas]** lista o conjunto completo de plataformas com suporte neste formulário. Cada entrada de plataforma consiste no **prefixo Platform.** _cadeia_ de caracteres ,  _onde cadeia de_ caracteres é um código de cadeia de caracteres arbitrário para a plataforma. Cada cadeia de caracteres corresponde à **entrada da CPU** de uma seção **[Plataformas]** individuais. Cada entrada em uma **seção [Plataformas]** define uma  _cadeia_ de caracteres de plataforma que faz referência a uma **[plataforma] subsequente.** _cadeia de caracteres_ **de plataforma ]** conforme mostrado aqui. 
  
**[Plataformas]**
  
**Plataforma**. _string_  =   _cadeia de caracteres de plataforma_
  
A seguir está um exemplo de **uma seção [Plataformas].** 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

Cada **uma [plataforma.** _cadeia de caracteres_ de plataforma **]** contém as duas entradas necessárias, **CPU** e **OSVersion**. A entrada da **CPU** especifica o processador e a **entrada osVersion** especifica o sistema operacional. Os **valores válidos** da CPU são descritos na tabela a seguir. 
  
|**Entrada da CPU**|**Processador**|
|:-----|:-----|
|Ix86  <br/> |Processadores de série Intel 80x86 e Pentium, bem como processadores equivalentes da AMD, Cyila, NextGen e outros fabricantes.  <br/> |
|MIPS  <br/> |Processadores de série MIPS R4000.  <br/> |
|AXP  <br/> |Processador Digital Equipment Corporation Alpha AXP.  <br/> |
|PPC  <br/> |Processadores de séries Do Power PC.  <br/> |
|M68  <br/> |Processadores de séries 68x00 Dalmárola.  <br/> |
   
Os **valores válidos** do OSVersion são descritos na tabela a seguir. 
  
|**Entrada OSVersion**|**Sistema Operacional**|
|:-----|:-----|
|Win3.1  <br/> |Windows 3.1 e Windows for Workgroups 3.11.  <br/> |
|WinNT3.5  <br/> |Windows NT 3.5 ou inferior.  <br/> |
|Win95  <br/> |Windows 95.  <br/> |
|WinNT4.0  <br/> |Windows NT 4.0.  <br/> |
|Mac7  <br/> |Macintosh System 7.  <br/> |
   
Além disso, a **[Plataforma.** _cadeia de caracteres_ de plataforma **]** section must contain either a **File** or **LinkTo** entry. A **entrada Arquivo** lista o arquivo executável do aplicativo do servidor de formulário que a biblioteca de formulário mantém e carrega em um novo subdiretório no cache de disco quando o formulário é lançado. Se uma **entrada LinkTo** for usada, ela conterá o nome de uma cadeia de caracteres de plataforma diferente da qual as informações **de** arquivo são retiradas. Isso será útil se uma versão de um formulário suportar várias plataformas. 
  
A **entrada do Registro**  é usada sempre que a entrada de arquivo é usada, ela identifica a chave do Registro para a biblioteca de formulário onde o arquivo executável para o aplicativo de servidor de formulário é armazenado. As cadeias de caracteres precedidas por uma invertida ( \ ) são colocadas na raiz do registro. Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form. Os caracteres "%d" podem ser usados para indicar o nome do caminho do diretório do qual o arquivo de configuração de formulário foi lido. Isso é útil para especificar outros arquivos com nomes de caminho relativos ao arquivo de configuração do formulário. **Várias entradas** de **Arquivo** ou registro podem ser especificadas usando Arquivo ou Registro como um prefixo seguido por qualquer outro texto. O formato para a **[plataforma.** _cadeia de caracteres_ **de plataforma ]** seção é: 
  
- **[Plataforma.** _cadeia de caracteres de_ **plataforma ]**
    
- **CPU**  =   _string_
    
- **OSVersion**  =   _string_
    
- **Arquivo**  =   _path_
    
- **LinkTo**  =   _string_
    
- **Registro**  =   _string_
  
A seguir estão dois **exemplos [Platform.** _cadeia de caracteres_ de plataforma **]** , uma usando a **entrada de** arquivo e outra usando a entrada **LinkTo.** 
  
```cpp
[Platform.NTx86]
CPU = ix86
OSVersion = WinNT3.5
File = \helpdesk.exe
Registry = Local Server = %d\helpdesk.exe
[Platform.Win95]
CPU = ix86
OSVersion = Win95
LinkTo = NTx86

```

A **[plataforma.** _cadeia_ de caracteres de plataforma **]** seção é ignorada ao adicionar um formulário à biblioteca de formulário local, quando é assumido que o instalador colocou os arquivos que estão transformando o manipulador de classe de mensagem em armazenamento local disponível conforme nomeado na seção do manipulador no registro OLE e fez o registro OLE no registro do sistema. 
  

