---
title: Visão geral de interface e objeto MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fcd85bf518f4e6466bf15a09e417767bc34df78d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345784"
---
# <a name="mapi-object-and-interface-overview"></a>Visão geral de interface e objeto MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um objeto MAPI é uma classe de objeto C++ ou estrutura de dados C herdada de uma ou mais interfaces MAPI ou conjuntos de funções relacionadas. Esses conjuntos de funções relacionadas são conhecidos por desenvolvedores do C++ como funções virtuais puras. Para uma função virtual pura, o MAPI fornece apenas o protótipo de função, não uma implementação. É esperado que um aplicativo cliente, um provedor de serviços ou MAPI forneça essa implementação criando uma classe de objeto que herda da interface e está em conformidade com as descrições de funções da API de mensagens. Uma interface MAPI pode ser instanciada apenas por meio de uma classe herdada.
  
Há vários objetos MAPI diferentes, cada objeto herdado de uma interface que é basicamente herdada da interface [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) . **IUnknown** é a interface base do modelo de objeto do componente OLE (com). Ele fornece objetos MAPI com um mecanismo padrão para comunicação e controle. COM dita como os implementadores de objetos lidam com problemas como gerenciamento de memória, gerenciamento de parâmetros e multithreading. Ao estar de acordo com esse modelo, um implementador de objeto obedece a um contrato conforme especificado pelas interfaces incluídas no objeto. 
  
Muitas interfaces MAPI são herdadas diretamente de **IUnknown**, enquanto outras são herdadas indiretamente por uma das duas outras interfaces base: [IMAPIProp: IUnknown](imapipropiunknown.md) para gerenciamento de propriedades e [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) para pasta e acesso ao catálogo de endereços. As interfaces base nunca são implementadas como objetos autônomos separados; Eles são sempre implementados como parte de outros objetos, objetos que implementam interfaces derivadas. 
  
O MAPI define vários tipos de objetos, cada um deles implementado por um ou mais componentes MAPI. Os objetos implementados por clientes são usados por MAPI, por provedores de serviços e por componentes de formulário personalizados. Os objetos implementados por provedores de serviço normalmente são usados por MAPI e por clientes. Os objetos implementados por provedores de biblioteca de formulários e servidores de formulário são usados por outros componentes de formulário e por clientes. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Conceitos de MAPI](mapi-concepts.md)

