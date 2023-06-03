---
layout: page
title: Diagrammes de composants
permalink: /diagrammes-de-composants/
nav_order: 4
has_children: true
has_toc: false
---


# Diagrammes de composants
Un **diagramme de composantes** présente une vue **statique** de **l'implémentation d'un système**.

## Représentation  
Une composante est une partie **physique** et **remplaçable** d'un système qui se conforme et réalise un ensemble d'interfaces.  
Une composante est **l'implémentation physique** de classes ou de paquetages.

![](/out/plant_uml/représentationComponentDiagram/représentationComponentDiagram.svg)

Les noms de composantes sont des noms tirés de **l'implémentation** du système. Par exemple, pour le diagramme ci-haut, on aurait pu avoir le code suivant: 
```
// ClientUI.java
public class ClientUI {
    private ProductAPI productAPI;
    
    public void setProductAPI(ProductAPI productAPI) {
        this.productAPI = productAPI;
    }
    
    // Méthodes pour l'interface utilisateur de la boutique en ligne
    // ...
}

// ProductAPI.java
public class ProductAPI {
    private OrderService orderService;
    private PaymentService paymentService;
    
    public void setOrderService(OrderService orderService) {
        this.orderService = orderService;
    }
    
    public void setPaymentService(PaymentService paymentService) {
        this.paymentService = paymentService;
    }
    
    // Méthodes pour accéder aux informations sur les produits
    // ...
}

// OrderService.java
public class OrderService {
    private ProductAPI productAPI;
    
    public void setProductAPI(ProductAPI productAPI) {
        this.productAPI = productAPI;
    }
    
    // Méthodes pour gérer les commandes
    // ...
}

// PaymentService.java
public class PaymentService {
    // Méthodes pour gérer les paiements
    // ...
}
```
## Relations

## Dépendances

## Vues