---
title: Objeto MAPI e visão geral da Interface
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fcd85bf518f4e6466bf15a09e417767bc34df78d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390986"
---
# <a name="mapi-object-and-interface-overview"></a>Objeto MAPI e visão geral da Interface

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um objeto MAPI é uma classe de objeto C++ ou a estrutura de dados C herdadas de uma ou mais interfaces MAPI ou conjuntos de funções relacionadas. Essas coleções de funções relacionadas são conhecidas para desenvolvedores do C++ como funções virtuais puras. Para uma função essencialmente virtual MAPI fontes somente o protótipo de função, não uma implementação. Espera-se que um aplicativo cliente, um provedor de serviços ou MAPI fornecerá essa implementação criando uma classe de objeto que herda da interface e está em conformidade com as descrições de função da API de mensagens. Uma interface MAPI pode ser instanciada apenas por meio de uma classe herdada.
  
Há muitos objetos MAPI diferentes, cada objeto que herda de uma interface que é basicamente herdada da interface [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) . **IUnknown** é a interface de base OLE COM Component Object Model (). Ele fornece objetos MAPI com um mecanismo padrão para comunicação e controle. COM dita como implementadores do objeto lidar com problemas, como gerenciamento de memória, gerenciamento de parâmetro e multithreading. Conforme esse modelo, Implementador de um objeto de acordo com um contrato conforme especificado pelas interfaces incluídos no objeto. 
  
Muitas interfaces MAPI são herdadas diretamente do **IUnknown**, enquanto outras são herdadas indiretamente por meio de uma das duas interfaces de base: [IMAPIProp: IUnknown](imapipropiunknown.md) para gerenciamento de propriedade e [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) para a pasta e acesso do catálogo de endereços. Interfaces base nunca são implementados como separado, objetos de autônomo; sempre são implementados como parte de outros objetos, derivado de objetos que implementam interfaces. 
  
MAPI define vários tipos de objetos, cada um implementado por um ou mais componentes MAPI. Objetos implementados por clientes são usados pelo MAPI, por provedores de serviços e pelos componentes do formulário personalizado. Objetos implementados pelos provedores de serviço geralmente são usados por MAPI e pelos clientes. Objetos implementada por provedores de biblioteca de formulário e servidores de formulário são usados por outros componentes do formulário e pelos clientes. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Conceitos MAPI](mapi-concepts.md)

