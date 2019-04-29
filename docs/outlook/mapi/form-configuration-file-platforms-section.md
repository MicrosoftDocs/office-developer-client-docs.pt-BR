---
title: Seção do arquivo de configuração de formulários [plataformas]
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
# <a name="form-configuration-file-platforms-section"></a>Seção do arquivo de configuração de formulários [plataformas]

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A seção **[plataformas]** lista o conjunto completo de plataformas suportadas por esse formulário. Cada entrada de plataforma consiste na plataforma de prefixo **.** _cadeia_de caracteres, onde _cadeia_ de caracteres é um código de cadeia de caracteres arbitrário para a plataforma. Cada cadeia de caracteres corresponde à entrada de **CPU** de uma individual **[Platforms]** seções. Cada entrada em uma seção **[Platforms]** define uma _cadeia de caracteres de plataforma_ que faz referência a um subseqüente **[Platform.** _cadeia de caracteres de plataforma_ **]** como mostrado aqui. 
  
A seção **[plataformas]** lista o conjunto completo de plataformas suportadas por esse formulário. Cada entrada de plataforma consiste na plataforma de prefixo **.** _cadeia_de caracteres, onde _cadeia_ de caracteres é um código de cadeia de caracteres arbitrário para a plataforma. Cada cadeia de caracteres corresponde à entrada de **CPU** de uma individual **[Platforms]** seções. Cada entrada em uma seção **[Platforms]** define uma _cadeia de caracteres de plataforma_ que faz referência a um subseqüente **[Platform.** _cadeia de caracteres de plataforma_ **]** como mostrado aqui. 
  
**Plataformas**
  
**Platform**. __ =  _cadeia_ de caracteres de plataforma de cadeia
  
Veja a seguir um exemplo de uma seção **[Platforms]** . 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

Cada **[Platform.** _cadeia de caracteres de plataforma_ **]** contém as duas entradas obrigatórias, **CPU** e **OSVersion**. A entrada de **CPU** especifica o processador e a entrada **OSVersion** especifica o sistema operacional. Valores de **CPU** válidos são descritos na tabela a seguir. 
  
|**Entrada de CPU**|**Processador**|
|:-----|:-----|
|Ix86  <br/> |Processadores Intel 80x86 e Pentium Series, bem como processadores equivalentes do AMD, Cyrix, NextGen e outros fabricantes.  <br/> |
|SEQÜENCIA  <br/> |Processadores da série MIPS R4000.  <br/> |
|AXP  <br/> |Processador Digital Equipment Corporation Alpha AXP.  <br/> |
|PPC  <br/> |Processadores da série Motorola Power PC.  <br/> |
|M68  <br/> |Processadores da série mororola 68x00.  <br/> |
   
Os valores de **OSVersion** válidos são descritos na tabela a seguir. 
  
|**Entrada de OSVersion**|**Sistema Operacional**|
|:-----|:-----|
|Win 3.1  <br/> |Windows 3,1 e Windows para Workgroups 3,11.  <br/> |
|WinNT 3.5  <br/> |Windows NT 3,5 ou inferior.  <br/> |
|Win95  <br/> |Windows 95.  <br/> |
|WinNT 4.0  <br/> |Windows NT 4,0.  <br/> |
|Mac7  <br/> |Sistema Macintosh 7.  <br/> |
   
Além disso, o **[Platform.** _cadeia de caracteres de plataforma_ **]** seção deve conter uma entrada de **arquivo** ou **linkto** . A entrada de **arquivo** lista o arquivo executável do aplicativo do servidor de formulário que a biblioteca de formulários mantém e carrega em um novo subdiretório no cache de disco quando o formulário é iniciado. Se for **** usada uma entrada de linkto, ela conterá o nome de uma cadeia de caracteres de plataforma diferente da qual as informações do **arquivo** foram realizadas. Isso será útil se uma versão de um formulário oferecer suporte a várias plataformas. 
  
A entrada **do registro** é usada sempre que a entrada de **arquivo** é usada, ela identifica a chave do registro para a biblioteca de formulários, onde o arquivo executável do aplicativo do servidor de formulário está armazenado. Cadeias de caracteres precedidas por uma barra invertida (\) são colocadas na raiz do registro. Cadeias de caracteres não precedidas por uma barra invertida são colocadas na chave HKEY_CLASSES_ROOT\CLSID\ _GUID_\ do registro, onde _GUID_ é o **GUID** do formulário. Os caracteres "% d" podem ser usados para indicar o nome do caminho do diretório a partir do qual o arquivo de configuração de formulário foi lido. Isso é útil para especificar outros arquivos com Pathnames relativos ao arquivo de configuração de formulário. **Várias** entradas de arquivo ou **registro** podem ser especificadas usando o arquivo ou registro como um prefixo seguido por qualquer outro texto. O formato para o **[Platform.** _cadeia de caracteres de plataforma_ **]** seção é: 
  
- **Plataforma.** _cadeia de caracteres de plataforma_ **]**
    
- **** =  _Cadeia de caracteres_ de CPU
    
- **** =  _Cadeia de caracteres_ OSVersion
    
- **** =  _Caminho_ do arquivo
    
- **** Cadeia de caracteres linkto__  =  
    
- **** =  _Cadeia de caracteres_ do registro
  
A seguir estão dois exemplos de **[Platform.** _cadeia de caracteres de plataforma_ **]** , uma usando a entrada de **arquivo** e outra usando a entrada **linkto** . 
  
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

O **[Platform.** _cadeia de caracteres de plataforma_ **]** seção é ignorada ao adicionar um formulário à biblioteca de formulários local, quando presume-se que o instalador colocou os arquivos constituting o manipulador de classe de mensagem no armazenamento local disponível como nomeado na seção do manipulador no registro OLE e fez o registro OLE no registro do sistema. 
  

