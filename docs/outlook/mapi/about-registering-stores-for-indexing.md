---
title: Sobre o registro de armazenamentos para indexação
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
# <a name="about-registering-stores-for-indexing"></a>Sobre o registro de armazenamentos para indexação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico é específico da Pesquisa Instantânea no Microsoft Office Outlook 2007.
  
A Pesquisa Instantânea permite que você encontre itens rapidamente no Outlook. Ele usa componentes do Windows Desktop Search.
  
O Manipulador de Protocolo MAPI verifica o Registro do Windows em busca de armazenamentos que ele deve indexar para fins de pesquisa. Os provedores da Loja que querem ser indexados devem ser registrados no Registro do Windows.
  
Por padrão, o Windows Desktop Search adiciona os seguintes quatro tipos de provedores de loja ao Registro do Windows para permitir a indexação:
  
- Armazenar arquivos de Pastas Particulares (. PST).
    
-  Microsoft Exchange store, including any Offline Folder files (.ost). 
    
-  Armazenar para pastas públicas. 
    
-  Store para Microsoft Office Outlook Connector para MSN. 
    
 Provedores de armazenamento de terceiros que querem ser indexados devem se registrar no Registro do Windows. 
  
> [!NOTE]
> Os administradores e usuários podem usar uma configuração de Política de Grupo para impedir que a Pesquisa da Área de Trabalho do Windows indexe itens do Outlook. Para obter mais informações, consulte [Estendendo a Pesquisa da Área de Trabalho do Windows.](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx) 
  
## <a name="registry-keys"></a>Chaves do Registro

Em um computador, todos os provedores de armazenamento que deseja indexar devem ser registrados em apenas uma das três chaves de registro a seguir no Registro do Windows. O Manipulador de Protocolo MAPI analisa cada uma dessas chaves na seguinte ordem:
  
1. [HKLM]\Software\Policies\Microsoft\Windows\Windows Search\
    
2. [HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\
    
3. [HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\
    
 Cada valor sob a chave corresponde a um provedor de armazenamento que seria indexado. O nome do valor é o IDENTIFICADOr Global Exclusivo (GUID) do provedor de armazenamento, que é do tipo **DWORD** e tem o valor hexadecimal 0x00000001. 
  
## <a name="guids-for-store-providers"></a>GUIDs for Store Providers

A propriedade MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** especifica o GUID de um armazenamento MAPI. Os GUIDs para os provedores de armazenamento que os índices do Outlook estão descritos na tabela a seguir. 
  
||||
|:-----|:-----|:-----|
|**Tipo de Provedor de Armazenamento** <br/> |**GUID** <br/> |**Anotações** <br/> |
|Arquivos de Pastas Particulares (. PST)  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |O GUID está documentado no arquivo de header público mspst.h **como MSPST_UID_PROVIDER** <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |O GUID está documentado no arquivo de cabeça público edkmdb.h como **pbExchangeProviderPrimaryUserGuid** <br/> |
|Pastas públicas  <br/> |{70fab278-f7af-cd11-9bc8-00aa002fc45a}  <br/> |O GUID está documentado no arquivo de título público edkmdb.h como **pbExchangeProviderPublicGuid** <br/> |
|Conector do Outlook para MSN  <br/> |{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}  <br/> |Nenhum  <br/> |
   
## <a name="see-also"></a>Confira também



[Sobre a API de Armazenamento](about-the-store-api.md)

