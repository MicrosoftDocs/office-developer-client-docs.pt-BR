---
title: Sobre a resolução de conflitos de tipos de itens personalizados
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 3f0853fc-f9f2-4314-ac55-47fe1e52d019
description: Este tópico descreve como resolver conflitos de tipos de item personalizados criados no Outlook.
ms.openlocfilehash: 357dd9182f26c4e9e1e264afdee296859e7b3483
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382985"
---
# <a name="about-conflict-resolution-for-custom-item-types"></a>Sobre a resolução de conflitos de tipos de itens personalizados

Este tópico descreve como resolver conflitos de tipos de item personalizados criados no Outlook.
  
## <a name="conflict-resolution-for-standard-outlook-item-types"></a>Resolução de conflitos de tipos de item padrão do Outlook

No Outlook, os conflitos ocorrem quando duas ou mais cópias do mesmo item são modificadas separadamente. O Outlook detecta conflitos durante a sincronização. Por exemplo, você pode atualizar um item de reunião online no Outlook Web App e atualizar o mesmo item de reunião no Outlook enquanto trabalha offline. Quando o Outlook ficar online novamente e sincronizar os dados entre o computador cliente e o servidor, ele detectará que existem duas cópias diferentes do mesmo item de reunião.
  
Quando o Outlook sincronizar itens que pertençam a um tipo de item padrão do Outlook, ele leva em consideração as propriedades que são específicas para esse tipo de item para detectar possíveis conflitos. O Outlook tenta resolver conflitos e armazena a cópia resultante na pasta apropriada sem solicitar intervenção do usuário. Em casos onde o Outlook considera que há uma possibilidade de que a cópia resultante não contenha todos os dados essenciais, ele armazena cópias conflitantes na pasta Conflitos dentro da pasta Problemas de Sincronização. 
  
> [!NOTE]
> Problemas de Sincronização e suas subpastas ficam ocultos até você clicar em **Lista de Pastas** no Painel de Navegação. 
  
Nesses casos, os usuários podem escolher ir para pasta Conflitos para verificar quais itens estiveram em conflito e se desejam usar uma cópia na pasta Conflitos para substituir a cópia que o Outlook decidiu manter.
  
## <a name="conflict-resolution-for-custom-item-types"></a>Resolução de conflitos de tipos de item personalizados

### <a name="item-types-and-message-classes"></a>Tipos de item e classes de mensagens
  
Todos os itens no Outlook são associados a uma classe da mensagem. Por exemplo, por padrão, um item de email está associado à classe de mensagem **IPM.Note**. A classe de mensagem é usada principalmente para identificar o formulário que deve ser usado para exibir o item no Outlook. O Outlook dá suporte a uma lista de classes de mensagens que são mapeadas para os tipos de itens criados no Outlook. Para saber mais sobre classes de mensagens, confira [Tipos de item e classes de mensagens](https://msdn.microsoft.com/library/15b709cc-7486-b6c7-88a3-4a4d8e0ab292%28Office.15%29.aspx). 
  
Os usuários podem criar tipos de item personalizados, atribuir classes de mensagem personalizadas aos tipos de itens personalizados, e fazer com que o Outlook use um formulário personalizado para exibir os tipos de itens personalizados. Por exemplo, talvez você queira que o Outlook exiba um formulário de contato comercial personalizado para seus contatos comerciais. Para fazer isso, você pode criar uma classe de mensagem **IPM.Contact.Business** personalizada, criar um formulário personalizado para essa classe de mensagem e atribuir contatos comerciais à classe de mensagem. 
  
### <a name="registering-a-conflict-resolution-scheme-for-custom-item-types"></a>Registrar um esquema de resolução de conflitos para tipos de item personalizados
  
Quando você cria um tipo de item personalizado que não seja a classe de mensagem personalizada e o formulário personalizado, você deve considerar como deseja que o Outlook lide com conflitos entre cópias de um item desse tipo de item. Por padrão, o Outlook emprega um esquema de resolução comum a todos os itens, não considera propriedades específicas a um tipo de item e apresenta cópias conflitantes para o usuário tomar uma decisão. Isso ocorre porque os tipos de item personalizados podem definir campos personalizados no formulário personalizado e podem ter propriedades personalizadas e código personalizado. Se desejar que o Outlook considere propriedades específicas do item e tente resolver o conflito com intervenção mínima do usuário, você deverá especificar isso por meio de uma configuração no registro do Windows. Isso pode ser feito de uma das seguintes formas: 
  
- Aplicando uma configuração de Política de Grupo no computador local que define a chave do Registro ConflictMsgCls. O exemplo a seguir especifica a versão "14.0" para o Outlook 2010: 
  
   `[HKCU]\Software\Policies\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
- Ao modificar diretamente a chave do Registro do usuário ConflictMsgCls. O exemplo a seguir especifica a versão "14.0" para o Outlook 2010: 
  
   `[HKCU]\Software\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
Definir a resolução de conflitos por meio de uma Política de Grupo terá precedência sobre modificar diretamente a chave do Registro do usuário. A localização da chave no Registro depende da versão do Outlook. Você especifica o nome da classe de mensagem personalizada como um valor sob essa chave. Especifica o tipo de valor como **DWORD** e os dados do valor como um dos valores mostrados na tabela a seguir, dependendo do esquema de resolução escolhido. 
  
|Dados  | Descrição  |
|:-----|:-----|
|0  <br/> |Resolução de item comum que exige uma decisão de usuário, conforme usado no Outlook 2002 e em versões anteriores.  <br/> |
|1  <br/> |Resolução de item comum que exige intervenção mínima do usuário, conforme usado no Outlook desde o Outlook 2003.  <br/> |
|2  <br/> |Resolução específica para itens de email.  <br/> |
|3  <br/> |Resolução específica para itens de reunião.  <br/> |
|4  <br/> |Resolução específica para itens de compromisso.  <br/> |
|5  <br/> |Resolução específica para itens de contato.  <br/> |
|6  <br/> |Resolução específica para itens de tarefas.  <br/> |
|7  <br/> |Resolução específica para itens de notas autoadesivas.  <br/> |
|8  <br/> |Resolução específica para itens de diário.  <br/> |
   
Se você especificar um dos esquemas de resolução específicos de itens (dados de chave de 2 a 8), o Outlook tentará resolver conflitos em campos específicos de item (por exemplo, campos **Início** e **Fim** de um item de compromisso) automaticamente sem intervenção do usuário. Se o Outlook considerar que a resolução pode resultar em perda de dados essenciais, ele manterá cópias conflitantes na pasta Conflitos, e os usuários poderão escolher ir para a pasta Conflitos para resolver novamente esses itens de forma manual e substituir a resolução automática. 
  
Usando o mesmo exemplo de contatos comerciais acima, se você quiser especificar o esquema de resolução específico de itens de contato para a classe de mensagem personalizada **IPM.Contact.Business**, adicione-o como um valor **DWORD** sob `[HKCU]\Software\Microsoft\Office\15.0\Outlook\Options\ConflictMsgCls` e especifique 5 como os dados. 
  
> [!NOTE]
> O Outlook sempre usa um esquema de resolução específico para itens de compromisso de classes de mensagem personalizadas com base na classe de mensagem de compromisso, **IPM.Appointment** (por exemplo, **IPM.Appointment.Personal**). 
  
## <a name="see-also"></a>Confira também

- [Objetos de item do Outlook](https://msdn.microsoft.com/library/6ea4babf-facf-4018-ef5a-4a484e55153a%28Office.15%29.aspx)

