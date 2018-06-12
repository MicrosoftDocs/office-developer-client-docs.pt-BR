---
title: Sobre como registrar repositórios para indexação
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: b16446644c360185908e7f4e58463257fe17f403
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766110"
---
# <a name="about-registering-stores-for-indexing"></a>Sobre como registrar repositórios para indexação

  
  
**Aplica-se a**: Outlook 
  
Este tópico é específico para a pesquisa instantânea no Microsoft Office Outlook 2007.
  
Pesquisa instantânea permite localizar rapidamente os itens no Outlook. Ele usa os componentes do Windows Desktop Search.
  
O manipulador de protocolo MAPI verifica o registro do Windows para repositórios que ele deve indexar para fins de pesquisa. Provedores de armazenamento que devem ser indexados devem ser registrados no registro do Windows.
  
Por padrão, o Windows Desktop Search adiciona os seguintes quatro tipos de provedores de armazenamento no registro do Windows para permitir a indexação:
  
- Repositório de arquivos de pastas particulares (. PST).
    
-  Repositório do Microsoft Exchange, incluindo quaisquer arquivos de pasta Offline (. ost). 
    
-  Repositório para pastas públicas. 
    
-  Repositório para o Microsoft Office Outlook Connector para MSN. 
    
 Provedores de armazenamento de terceiros que devem ser indexados devem ser registrados no registro do Windows. 
  
> [!NOTE]
> Os administradores e usuários podem usar uma configuração de diretiva de grupo para impedir a indexação de itens do Outlook do Windows Desktop Search. Para obter mais informações, consulte [Estendendo o Windows Desktop Search](http://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx). 
  
## <a name="registry-keys"></a>Chaves do registro

Em um computador, todos os provedores de armazenamento que devem ser indexados devem ser registrados em apenas um dos seguintes chaves de registro de três no registro do Windows. O manipulador de protocolo MAPI procura sob cada uma dessas chaves na seguinte ordem:
  
1. \Software\Policies\Microsoft\Windows\Windows Search\ [HKLM]
    
2. \Software\Microsoft\Windows\Windows Search\Preferences\ [HKLM]
    
3. \Software\Microsoft\Windows\Windows Search\Preferences\ [HKCU]
    
 Cada valor na chave corresponde a um provedor de repositório que seria indexado. O nome do valor é o identificador global exclusivo (GUID) o provedor de armazenamento, que é do tipo **DWORD** e tem o valor hexadecimal 0x00000001. 
  
## <a name="guids-for-store-providers"></a>GUIDs de provedores de armazenamento

A propriedade MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** Especifica o GUID de um repositório MAPI. Os GUIDs para os provedores de armazenamento que os índices do Outlook estão descritos na tabela a seguir. 
  
||||
|:-----|:-----|:-----|
|**Tipo de provedor de armazenamento** <br/> |**GUID** <br/> |**Notes** <br/> |
|Arquivos de pastas particulares (. PST)  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |GUID documentada a mspst.h do arquivo de cabeçalho público como **MSPST_UID_PROVIDER** <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |GUID documentada o arquivo de cabeçalho público Edkmdb. h como **pbExchangeProviderPrimaryUserGuid** <br/> |
|Pastas públicas  <br/> |{70fab278-f7af-cd11-9bc8-00aa002fc45a}  <br/> |GUID documentada o arquivo de cabeçalho público Edkmdb. h como **pbExchangeProviderPublicGuid** <br/> |
|O Outlook Connector para MSN  <br/> |{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}  <br/> |Nenhum  <br/> |
   
## <a name="see-also"></a>Ver também



[Sobre o API de armazenamento](about-the-store-api.md)

