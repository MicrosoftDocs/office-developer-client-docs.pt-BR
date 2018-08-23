---
title: Instalar o subsistema MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: adb4d09ccce95683ac46e7b271fafa328b1a9f97
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575347"
---
# <a name="installing-the-mapi-subsystem"></a>Instalar o subsistema MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Versões suportadas do Windows instalem a biblioteca de stub MAPI, Mapi32, no _ \<unidade\>_ \Windows\System32 folder. 
  
As versões com suporte do Windows são:
  
- Windows 7.
    
- Windows Vista.
    
- Windows Server 2008.
    
- Windows Server 2003.
    
- Windows XP.
    
Para instalar corretamente o subsistema de MAPI, instale um aplicativo que contém um subsistema baseado em MAPI, como o Microsoft Outlook.
  
Você pode encontrar informações sobre a instalação do subsistema MAPI do computador no registro do sistema. Todos os valores nas entradas de registro são cadeias de caracteres. 
  
Programas de instalação do serviço de mensagem são responsáveis por criar as informações de instalação na seguinte chave de registro do sistema: 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
Serviços de mensagem devem adicionar entradas do registro do sistema. 
  
A tabela a seguir resume como clientes recuperam informações de versão para o subsistema MAPI em seus computadores.
  
|**Para verificar**|**Registry**|
|:-----|:-----|
|Disponibilidade de MAPI  <br/> |Procure por `MAPIX=1`.  <br/> |
|Versão disponível de MAPI  <br/> |Procure por uma cadeia de caracteres MAPIXVER do formulário " _x.x.x_".  <br/> |
   
## <a name="see-also"></a>Confira também



[Vis�o geral da programa��o MAPI](mapi-programming-overview.md)

