---
title: Instalar o subsistema MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: 'Última modificação: 9 de março de 2015'
localization_priority: Priority
ms.openlocfilehash: 112a683f5967f8740c2d21285eb4ebbc0f455c48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309636"
---
# <a name="installing-the-mapi-subsystem"></a>Instalar o subsistema MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As versões com suporte do Windows instalam a biblioteca stub do MAPI, Mapi32.dll, na pasta  _\<drive\>_ \Windows\System32. 
  
As versões com suporte do Windows são as seguintes:
  
- Windows 7.
    
- Windows Vista.
    
- Windows Server 2008.
    
- Windows Server 2003.
    
- Windows XP.
    
Para instalar corretamente o subsistema MAPI, instale um aplicativo que contenha um subsistema baseado em MAPI, como o Microsoft Outlook.
  
Você pode encontrar informações sobre a instalação de subsistema MAPI do computador no registro do sistema. Todos os valores das entradas de registro são cadeias de caracteres. 
  
Os programas de instalação do serviço de mensagens são responsáveis por criar as informações de instalação na seguinte chave de registro do sistema: 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
Os serviços de mensagem devem adicionar entradas ao registro do sistema. 
  
A tabela a seguir resume a forma como os clientes recuperam informações de versão para o subsistema MAPI em seus computadores.
  
|**Para verificar**|**Registro**|
|:-----|:-----|
|Disponibilidade de MAPI  <br/> |Procure  `MAPIX=1`.  <br/> |
|Versão de MAPI disponível  <br/> |Procure uma cadeia de caracteres MAPIXVER do formulário " _x.x.x_".  <br/> |
   
## <a name="see-also"></a>Confira também



[Visão geral da programação MAPI](mapi-programming-overview.md)

