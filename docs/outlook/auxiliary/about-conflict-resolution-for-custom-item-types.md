---
title: Sobre a resolução de conflitos de tipos de itens personalizados
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 3f0853fc-f9f2-4314-ac55-47fe1e52d019
description: Este tópico descreve como resolver conflitos para tipos de item personalizada que você criar no Outlook.
ms.openlocfilehash: d85c2022d909901c71c20214f91b316cce81c596
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765780"
---
# <a name="about-conflict-resolution-for-custom-item-types"></a>Sobre a resolução de conflitos de tipos de itens personalizados

Este tópico descreve como resolver conflitos para tipos de item personalizada que você criar no Outlook.
  
## <a name="conflict-resolution-for-standard-outlook-item-types"></a>Resolução de conflito para tipos de item padrão do Outlook

No Outlook, os conflitos ocorrem quando dois ou mais cópias do mesmo item foram modificadas independentemente uns dos outros. Outlook detecta conflitos durante a sincronização. Por exemplo, você pode atualizar um item de reunião online no Outlook Web App e atualize o mesmo item de reunião no Outlook quando você trabalhar offline. Quando o Outlook vai online novamente e sincroniza os dados entre o computador cliente e o servidor, ele detecta que não existem duas cópias diferentes do mesmo item de reunião.
  
Quando o Outlook sincroniza os itens que pertencem a um tipo de item padrão do Outlook, que leva em consideração as propriedades que são específicas para esse tipo de item para detectar possíveis conflitos. O Outlook tenta resolver conflitos e armazena a cópia resultante na pasta apropriada sem solicitar a intervenção do usuário. Em casos onde o Outlook considera que existe uma possibilidade de que a cópia resultante não pode conter todos os dados essenciais, o Outlook armazena as cópias conflitantes na pasta conflitos, sob a pasta problemas de sincronização. 
  
> [!NOTE]
> Problemas de sincronização e suas subpastas estão ocultas até você clicar em **Lista de pastas** no painel de navegação. 
  
Nesses casos, os usuários podem escolher ir até a pasta conflitos para verificar quais itens foram em conflito e se usará uma cópia na pasta conflitos para substituir a cópia que Outlook decidiu reter.
  
## <a name="conflict-resolution-for-custom-item-types"></a>Resolução de conflito para tipos de item personalizada

### <a name="item-types-and-message-classes"></a>Tipos de item e classes de mensagens
  
Todos os itens do Outlook estão associados uma classe de mensagem. Por exemplo, por padrão, um item de email é associado a classe de mensagem **IPM. Observação**. A classe da mensagem é usada principalmente para identificar o formulário que deve ser usado para exibir o item no Outlook. Outlook oferece suporte a uma lista das classes de mensagem que são mapeados para os tipos de itens feitas no Outlook. Para saber mais sobre classes de mensagens, confira [Tipos de itens e classes de mensagens](http://msdn.microsoft.com/library/15b709cc-7486-b6c7-88a3-4a4d8e0ab292%28Office.15%29.aspx). 
  
Os usuários podem criar tipos de item personalizada, atribuir classes de mensagem personalizada para os tipos de item personalizada e fazer com que o Outlook use um formulário personalizado para exibir os tipos de item personalizada. Por exemplo, você talvez prefira Outlook para exibir um formulário de contato comercial personalizado para seus contatos comerciais. Para fazer isso, você pode criar uma classe de mensagem personalizada **IPM. Contact.Business**, crie um formulário personalizado para essa classe de mensagem e atribuir contatos comerciais com essa classe de mensagem. 
  
### <a name="registering-a-conflict-resolution-scheme-for-custom-item-types"></a>Registrando um esquema de resolução de conflito para tipos de item personalizada
  
Quando você cria um tipo de item personalizada, que não seja a classe de mensagem personalizada e o formulário personalizado, você também deve considerar como você gostaria que o Outlook para lidar com conflitos entre as cópias de um item desse tipo de item. Por padrão, o Outlook emprega um esquema de resolução comuns a todos os itens, não considera propriedades que são específicas para um tipo de item e apresenta conflitantes cópias para o usuário a tomar uma decisão. Isso ocorre porque os tipos de item personalizada podem definir os campos personalizados no formulário personalizado e podem ter propriedades personalizadas e código personalizado. Se desejar que o Outlook considerar propriedades específicas do item e tentar resolver o conflito com intervenção mínima do usuário, você deve especificar que por meio de uma configuração no registro do Windows. Isso pode ser obtido de uma das duas maneiras: 
  
- Aplicando uma configuração de diretiva de grupo no computador local, que define a chave do registro ConflictMsgCls. O exemplo a seguir especifica que a versão "14.0" para o Outlook 2010: 
  
   `[HKCU]\Software\Policies\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
- Modificando diretamente a chave de registro de usuário ConflictMsgCls. O exemplo a seguir especifica que a versão "14.0" para o Outlook 2010: 
  
   `[HKCU]\Software\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
Definindo a resolução de conflito por meio da diretiva de grupo prevalece sobre modificando diretamente a chave de registro do usuário. O local da chave no registro depende da versão do Outlook. Você pode especificar o nome da classe de mensagem personalizado como um valor sob essa chave. Especifique o tipo do valor como **DWORD**e os dados do valor como um dos valores mostrados na tabela a seguir, dependendo do esquema de resolução escolhido. 
  
|Data  | Descrição  |
|:-----|:-----|
|0  <br/> |Resolução de item comum que requer uma decisão do usuário, conforme usado no Outlook 2002 e versões anteriores.  <br/> |
|1  <br/> |Resolução de item comum que requer intervenção mínima do usuário, conforme usado no Outlook desde o Outlook 2003.  <br/> |
|2  <br/> |Resolução específica para itens de email.  <br/> |
|3  <br/> |Resolução específica aos itens da reunião.  <br/> |
|4  <br/> |Resolução específica aos itens de compromisso.  <br/> |
|5  <br/> |Resolução específica para itens de contato.  <br/> |
|6  <br/> |Resolução específica para itens de tarefa.  <br/> |
|7  <br/> |Resolução específica aos itens de nota.  <br/> |
|8  <br/> |Resolução específica aos itens de diário.  <br/> |
   
Se você especificar um dos esquemas de resolução de item específico (principais dados de 2 a 8), o Outlook tentará resolver conflitos nos campos de item específico (por exemplo, campos de **início** e **término** de um item de compromisso) automaticamente sem a intervenção do usuário . Se o Outlook considera que a resolução pode resultar em perda de dados essenciais, Outlook manterão conflitantes cópias na pasta conflitos e os usuários podem escolher ir até a pasta conflitos novamente resolver esses itens manualmente e substituir automático resolução. 
  
Usando o mesmo exemplo de contatos de negócios acima, se você deseja especificar o esquema de resolução de específicas de itens de contato para a classe de mensagem personalizada **IPM. Contact.Business**, você pode adicioná-lo como um valor **DWORD** em `[HKCU]\Software\Microsoft\Office\15.0\Outlook\Options\ConflictMsgCls`e especificar 5 como os dados. 
  
> [!NOTE]
> O Outlook sempre usa um esquema de resolução que é específico para itens de compromisso para classes de mensagem personalizada que se baseiam na classe de mensagem de compromisso, **IPM. Compromisso** (por exemplo, **IPM. Appointment.Personal**). 
  
## <a name="see-also"></a>Confira também

- [Objetos de item do Outlook](http://msdn.microsoft.com/library/6ea4babf-facf-4018-ef5a-4a484e55153a%28Office.15%29.aspx)

