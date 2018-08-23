---
title: Seção do arquivo de configuração de formulários [Plataformas]
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d86edfb6fcc72c5968a8ff5d9cd739e20e5dec43
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589893"
---
# <a name="form-configuration-file-platforms-section"></a>Seção do arquivo de configuração de formulários [Plataformas]

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A seção **[plataformas]** lista o conjunto completo de plataformas suportadas por este formulário. Cada entrada de plataforma consiste o prefixo **plataforma.** _cadeia de caracteres_, onde a _cadeia de caracteres_ é um código de cadeia de caracteres arbitrária para a plataforma. Cada sequência corresponde à entrada de **CPU** de um seções **[plataformas]** individuais. Cada entrada em uma seção **[plataformas]** define uma _cadeia de caracteres de plataforma_ que faz referência a um subsequentes **[Platform.** _cadeia de caracteres de plataforma_ seção de **]** , conforme mostrado aqui. 
  
A seção **[plataformas]** lista o conjunto completo de plataformas suportadas por este formulário. Cada entrada de plataforma consiste o prefixo **plataforma.** _cadeia de caracteres_, onde a _cadeia de caracteres_ é um código de cadeia de caracteres arbitrária para a plataforma. Cada sequência corresponde à entrada de **CPU** de um seções **[plataformas]** individuais. Cada entrada em uma seção **[plataformas]** define uma _cadeia de caracteres de plataforma_ que faz referência a um subsequentes **[Platform.** _cadeia de caracteres de plataforma_ seção de **]** , conforme mostrado aqui. 
  
**[Plataformas]**
  
**Plataforma**. _cadeia de caracteres_ =  _cadeia de caracteres de plataforma_
  
A seguir está um exemplo de uma seção **[plataformas]** . 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

Cada **[Platform.** _cadeia de caracteres de plataforma_ seção de **]** contém as duas entradas necessárias, **CPU** e **OSVersion**. A entrada de **CPU** Especifica o processador e a entrada de **OSVersion** Especifica o sistema operacional. Os valores válidos de **CPU** são descritos na tabela a seguir. 
  
|**Entrada de CPU**|**Processador**|
|:-----|:-----|
|Ix86  <br/> |Intel 80 x86 e processadores Pentium da série, bem como processadores de equivalentes da AMD, Cyrix, NextGen e outros fabricantes.  <br/> |
|MIPS  <br/> |Processadores MIPS R4000 da série.  <br/> |
|AXP  <br/> |Processador de equipamento Corporation Alpha AXP digital.  <br/> |
|PPC  <br/> |Processadores da série Motorola Power PC.  <br/> |
|M68  <br/> |Processadores Mororola 68 x 00 da série.  <br/> |
   
Os valores válidos de **OSVersion** são descritos na tabela a seguir. 
  
|**Entrada de OSVersion**|**Sistema Operacional**|
|:-----|:-----|
|Win 3.1  <br/> |Windows 3.1 e Windows para grupos de trabalho 3.11.  <br/> |
|WinNT3.5  <br/> |Windows NT 3.5 ou inferior.  <br/> |
|Win95  <br/> |Windows 95.  <br/> |
|Winnt 4.0  <br/> |Windows NT 4.0.  <br/> |
|Mac7  <br/> |Sistema 7 para Macintosh.  <br/> |
   
Além disso, o **[Platform.** _cadeia de caracteres de plataforma_ seção **]** deve conter uma entrada de um **arquivo** ou o **LinkTo** . A entrada de **arquivo** lista formulário server arquivo executável do aplicativo que a biblioteca de formulários mantém e carrega em um novo subdiretório no cache de disco quando o formulário for aberto. Se uma entrada de **LinkTo** for usada em vez disso, ele contém o nome de uma cadeia de caracteres de plataforma diferente da qual as informações do **arquivo** são obtidas. Isso é útil se uma versão de um formulário oferece suporte a várias plataformas. 
  
A entrada **do registro** é utilizada sempre que a entrada de **arquivo** é usada, ele identifica a chave do registro para a biblioteca de formulários, onde o arquivo executável para o aplicativo de servidor do formulário está armazenado. As cadeias de caracteres precedidas por uma barra invertida (\) são colocadas na raiz do registro. As cadeias de caracteres não precedidas por uma barra invertida são colocadas na HKEY_CLASSES_ROOT\CLSID\ _GUID_\ chave do registro, onde _GUID_ é o **GUID** do formulário. Os caracteres "%d" podem ser usados para indicar o nome do caminho do diretório do qual o arquivo de configuração de formulário foi lido. Isso é útil para especificar outros arquivos com nomes de caminhos em relação ao arquivo de configuração de formulário. Entradas de **Vários arquivos** ou **do registro** podem ser especificadas usando o arquivo ou do registro como um prefixo seguido de qualquer outro texto. O formato para o **[Platform.** _cadeia de caracteres de plataforma_ seção **]** é: 
  
- **[Platform.** _cadeia de caracteres de plataforma_ **]**
    
- **CPU** =  _cadeia de caracteres_
    
- **OSVersion** =  _cadeia de caracteres_
    
- **Arquivo** =  _caminho_
    
- **LinkTo** =  _cadeia de caracteres_
    
- **Registro** =  _cadeia de caracteres_
  
A seguir estão dois exemplos **[Platform.** _cadeia de caracteres de plataforma_ **]** seções, um usando a entrada de **arquivo** e um usando a entrada **LinkTo** . 
  
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

O **[Platform.** _cadeia de caracteres de plataforma_ seção **]** é ignorada quando a adição de um formulário para a biblioteca de formulários locais, quando supõe-se que o instalador colocou os arquivos que constitui o manipulador de classe de mensagem no armazenamento local disponível quando nomeados na seção do manipulador no registro do OLE e tiver feito o registro OLE no registro do sistema. 
  

