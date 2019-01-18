---
title: Folders
TOCTitle: Folders
ms:assetid: b72b5705-d77a-4cad-873d-457b9fb6553e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184634(v=office.15)
ms:contentKeyID: 55119856
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ecf342c54d1aa2020fbfad4175a220b2aefecbe3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707042"
---
# <a name="folders"></a>Folders

Esta seção fornece tarefas de exemplo que envolvem pastas. Objetos [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) representam a hierarquia de pastas onde os itens do Microsoft Outlook estão armazenados. Exemplos de pastas incluem as pastas Calendário, Emails e Itens Excluídos. No Assembly de Interoperabilidade Primário (PIA) do Outlook, membros do objeto **Folder** são expostos como membros do objeto [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)).

## <a name="in-this-section"></a>Nesta seção

|Tópico|Descrição|
|:----|:----------|
|[Adicionar uma pasta à lista de pastas](how-to-add-a-folder-to-the-folder-list.md) |Usar o método [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) para adicionar uma pasta à lista de pastas do Outlook.|
|[Enumerar pastas](how-to-enumerate-folders.md)  |Enumera pastas iterando um conjunto de pastas.|
|[Obter uma pasta padrão e enumerar suas subpastas](how-to-get-a-default-folder-and-enumerate-its-subfolders.md) |Obtém uma pasta padrão no repositório padrão do usuário e enumera suas subpastas.|
|[Obter uma pasta com base em seu caminho de pasta](how-to-get-a-folder-based-on-its-folder-path.md)  |Usa um caminho da pasta e obtém a pasta associada.|
|[Selecionar uma pasta e exibir informações de pasta](how-to-select-a-folder-and-display-folder-information.md)  |Exibe informações de forma programática sobre uma pasta que um usuário seleciona de uma lista de pastas especificada.|
|[Obter a classe de mensagens padrão de uma pasta](how-to-get-the-default-message-class-of-a-folder.md)  |Usa a propriedade [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) para obter a classe de mensagens padrão de uma pasta.|
|[Acessar dados específicos da solução armazenados como uma mensagem oculta em uma pasta ](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)  |Usa o objeto [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) para recuperar dados que estão armazenados como uma mensagem oculta de uma classe de mensagens específica em uma pasta.|
|[Certifique-se de que as propriedades de item personalizadas são compatíveis com consultas ao nível de pasta](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md) |Mostra como garantir que, ao adicionar uma propriedade personalizada a um tipo de item, você também adiciona a propriedade à pasta para que você pode consultar essa propriedade personalizada no nível da pasta.|

## <a name="see-also"></a>Confira também

- [Calendar](calendar.md)
- [Contacts](contacts.md)
- [Mail](mail.md)
- [Como faço para... (Referência do PIA do Outlook 2013)](how-do-i-outlook-2013-pia-reference.md)

