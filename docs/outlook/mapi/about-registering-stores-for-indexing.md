---
title: Sobre o registro de repositórios para indexação
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321823"
---
# <a name="about-registering-stores-for-indexing"></a>Sobre o registro de repositórios para indexação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico é específico para pesquisa instantânea no Microsoft Office Outlook 2007.
  
A pesquisa instantânea permite que você encontre itens rapidamente no Outlook. Ele usa componentes da pesquisa do Windows desktop.
  
O manipulador de protocolo MAPI verifica o registro do Windows em busca de armazenamentos que ele deve indexar para fins de pesquisa. Os provedores de repositórios que desejam ser indexados devem ser registrados no registro do Windows.
  
Por padrão, o Windows Desktop Search adiciona os quatro tipos de provedores de repositório a seguir ao registro do Windows para permitir a indexação:
  
- Armazenar para arquivos de pastas particulares (. PST).
    
-  Repositório do Microsoft Exchange, incluindo qualquer arquivo de pasta offline (. ost). 
    
-  Armazenar para pastas públicas. 
    
-  Store para o Microsoft Office Outlook Connector para MSN. 
    
 Provedores de repositório de terceiros que desejam ser indexados devem se registrar no registro do Windows. 
  
> [!NOTE]
> Administradores e usuários podem usar uma configuração de política de grupo para impedir que o Windows Desktop Search Pesquise itens do Outlook de indexação. Para obter mais informações, consulte esTendendo o [Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx). 
  
## <a name="registry-keys"></a>Chaves do registro

Em um computador, todos os provedores de repositórios que desejam ser indexados devem ser registrados em apenas uma destas três chaves do registro no registro do Windows. O manipulador de protocolo MAPI examina cada uma destas chaves na seguinte ordem:
  
1. [HKLM] pesquisa do \Software\Policies\Microsoft\Windows\Windows
    
2. [HKLM] \Software\Microsoft\Windows\Windows Search\Preferences\
    
3. [HKCU] \Software\Microsoft\Windows\Windows Search\Preferences\
    
 Cada valor abaixo da chave corresponde a um provedor de armazenamento que seria indexado. O nome do valor é o identificador global exclusivo (GUID) do provedor de repositório, que é do tipo **DWORD** e tem o valor hexadecimal 0x00000001. 
  
## <a name="guids-for-store-providers"></a>GUIDs para provedores de repositório

A propriedade MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** especifica o GUID de um repositório MAPI. Os GUIDs dos provedores de repositório que o Outlook indexa são descritos na tabela a seguir. 
  
||||
|:-----|:-----|:-----|
|**Tipo de provedor de repositório** <br/> |**GUID** <br/> |**Anotações** <br/> |
|Arquivos de pastas particulares (. PST  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |GUID está documentado no arquivo de cabeçalho público mspst. h as **MSPST_UID_PROVIDER** <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |GUID está documentado no arquivo de cabeçalho público edkmdb. h as **pbExchangeProviderPrimaryUserGuid** <br/> |
|Pastas públicas  <br/> |{70fab278-f7af-cd11-9bc8-00aa002fc45a}  <br/> |GUID está documentado no arquivo de cabeçalho público edkmdb. h as **pbExchangeProviderPublicGuid** <br/> |
|Outlook Connector para MSN  <br/> |{c34f5c97-eb05-bb4b-B199-2a7570ec7cf9}  <br/> |Nenhum  <br/> |
   
## <a name="see-also"></a>Confira também



[Sobre a API de Armazenamento](about-the-store-api.md)

