---
layout: default
title: "OS2borgerPc V3"
author: "Anna-Lis Berg"
date: "25-02-2025"
status: "Udkast" 
parent: "OS2borgerpc"
nav_order: 3
has_children: true
---

```mermaid
C4Context
     
           Boundary(b0, "", "") {

        Boundary(b1, "Lokal Git", "") {
        Container(spa, "Single Page Application", "javascript and angular", "Provides all the internet banking functionality to customers via their web browser.")
        }

        Boundary(b3, "Produkt anvenerer", "") {
        Person_Ext(personB, "Lokal driftsleverandør", "driftsleverandør til en anvenderkommune")
         }
        
        Boundary(b6, "NornNet", "") {
        Container(spa, "OS2specifikke tilpasninger til standard konfigurationen", "")
        System(SystemA, "BootC basis konfiguration", "")
     
       Rel(SystemA, spa, "")

          }
       

      }
 ```     