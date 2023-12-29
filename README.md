# E_cars
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <ctype.h>
#include <unistd.h>
#define MAX_CARS 100
#define MAX_HISTORY 100
typedef struct {
    int id;
    char brand[50];
    char model[50];
    char status[20];
} Car;
typedef struct {
    int carId;
    char rentDate[20];
    char returnDate[20];
    char email[50];
    char phoneNumber[15];
    char fullName[50];
    char idCardNumber[20];
    char paymentMethod[20];
    int rating;
} RentalHistory;
Car cars[MAX_CARS];
RentalHistory history[MAX_HISTORY];
int numCars = 0;
int numRentals = 0;
void initialiserVoituresDisponibles() {
    // Voiture 1
   strcpy(cars[numCars].brand, "Audi");
    strcpy(cars[numCars].model, "A3");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 2
    strcpy(cars[numCars].brand, "Audi");
    strcpy(cars[numCars].model, "A4");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 3
    strcpy(cars[numCars].brand, "Audi");
    strcpy(cars[numCars].model, "Q5");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 4
    strcpy(cars[numCars].brand, "Alfa Romeo");
    strcpy(cars[numCars].model, "Giulia");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 5
    strcpy(cars[numCars].brand, "Alfa Romeo");
    strcpy(cars[numCars].model, "Stelvio");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 6
    strcpy(cars[numCars].brand, "Alfa Romeo");
    strcpy(cars[numCars].model, "4C");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
     // Voiture 7
    strcpy(cars[numCars].brand, "BMW");
    strcpy(cars[numCars].model, "3 Series");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 8
    strcpy(cars[numCars].brand, "BMW");
    strcpy(cars[numCars].model, "5 Series");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 9
    strcpy(cars[numCars].brand, "BMW");
    strcpy(cars[numCars].model, "X5");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 10
    strcpy(cars[numCars].brand, "Bentley");
    strcpy(cars[numCars].model, "Continental GT");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 11
    strcpy(cars[numCars].brand, "Bentley");
    strcpy(cars[numCars].model, "Bentayga");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 12
    strcpy(cars[numCars].brand, "Bentley");
    strcpy(cars[numCars].model, "Mulsanne");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
     // Voiture 13
    strcpy(cars[numCars].brand, "Bugatti");
    strcpy(cars[numCars].model, "Veyron");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 14
    strcpy(cars[numCars].brand, "Bugatti");
    strcpy(cars[numCars].model, "Chiron");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 15
    strcpy(cars[numCars].brand, "Bugatti");
    strcpy(cars[numCars].model, "Divo");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
     // Voiture 15
    strcpy(cars[numCars].brand, "Lamborghini");
    strcpy(cars[numCars].model, "Aventador");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 16
    strcpy(cars[numCars].brand, "Lamborghini");
    strcpy(cars[numCars].model, "Huracán");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 17
    strcpy(cars[numCars].brand, "Lamborghini");
    strcpy(cars[numCars].model, "Urus");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 18
    strcpy(cars[numCars].brand, "Land Rover");
    strcpy(cars[numCars].model, "Range Rover");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 19
    strcpy(cars[numCars].brand, "Land Rover");
    strcpy(cars[numCars].model, "Discovery");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 20
    strcpy(cars[numCars].brand, "Land Rover");
    strcpy(cars[numCars].model, "Defender");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 21
    strcpy(cars[numCars].brand, "Mercedes-Benz");
    strcpy(cars[numCars].model, "C-Class");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 22
    strcpy(cars[numCars].brand, "Mercedes-Benz");
    strcpy(cars[numCars].model, "E-Class");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 23
    strcpy(cars[numCars].brand, "Mercedes-Benz");
    strcpy(cars[numCars].model, "GLE");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 24
    strcpy(cars[numCars].brand, "Mazda");
    strcpy(cars[numCars].model, "Mazda3");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 25
    strcpy(cars[numCars].brand, "Mazda");
    strcpy(cars[numCars].model, "Mazda6");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 26
    strcpy(cars[numCars].brand, "Mazda");
    strcpy(cars[numCars].model, "CX-5");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 27
    strcpy(cars[numCars].brand, "Nissan");
    strcpy(cars[numCars].model, "Altima");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 28
    strcpy(cars[numCars].brand, "Nissan");
    strcpy(cars[numCars].model, "Rogue");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 29
    strcpy(cars[numCars].brand, "Nissan");
    strcpy(cars[numCars].model, "GT-R");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 30
    strcpy(cars[numCars].brand, "Opel");
    strcpy(cars[numCars].model, "Astra");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 31
    strcpy(cars[numCars].brand, "Opel");
    strcpy(cars[numCars].model, "Corsa");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 31
    strcpy(cars[numCars].brand, "Volkswagen");
    strcpy(cars[numCars].model, "Golf");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 32
    strcpy(cars[numCars].brand, "Volkswagen");
    strcpy(cars[numCars].model, "Passat");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 33
    strcpy(cars[numCars].brand, "Volkswagen");
    strcpy(cars[numCars].model, "Tiguan");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 34
    strcpy(cars[numCars].brand, "Volvo");
    strcpy(cars[numCars].model, "XC60");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 35
    strcpy(cars[numCars].brand, "Volvo");
    strcpy(cars[numCars].model, "S60");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 36
    strcpy(cars[numCars].brand, "Volvo");
    strcpy(cars[numCars].model, "XC90");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
     // Voiture 37
    strcpy(cars[numCars].brand, "Yamaha");
    strcpy(cars[numCars].model, "YZF-R1");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 38
    strcpy(cars[numCars].brand, "Yamaha");
    strcpy(cars[numCars].model, "MT-07");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
    // Voiture 39
    strcpy(cars[numCars].brand, "Yamaha");
    strcpy(cars[numCars].model, "YXZ1000R");
    strcpy(cars[numCars].status, "Disponible");
    cars[numCars++].id = numCars;
}
void ajouterHistorique(int carId, const char *rentDate, const char *returnDate, const char *email, const char *phoneNumber, const char *fullName, const char *idCardNumber, const char *paymentMethod, int rating) {
    history[numRentals].carId = carId;
    strcpy(history[numRentals].rentDate, rentDate);
    strcpy(history[numRentals].returnDate, returnDate);
    strcpy(history[numRentals].email, email);
    strcpy(history[numRentals].phoneNumber, phoneNumber);
    strcpy(history[numRentals].fullName, fullName);
    strcpy(history[numRentals].idCardNumber, idCardNumber);
    strcpy(history[numRentals].paymentMethod, paymentMethod);
    history[numRentals].rating = rating;
    numRentals++;
}
void afficherMenu();
void listerVoituresDisponibles();
void louerVoiture();
void afficherDescriptionVoiture();
void supprimerVoitureDefaillante();
void modifierDetailsVoiture();
void afficherHistoriqueLocation();
void retournerVoiture();
void listerVoituresDisponiblesParLettre();
int main() {
    initialiserVoituresDisponibles();
    int choix;

    do {
        afficherMenu();
        printf("Entrez votre choix : ");
        scanf("%d", &choix);

        switch (choix) {
            case 1:
                listerVoituresDisponibles();
                break;
            case 2:
                louerVoiture();
                break;
            case 3:
                afficherDescriptionVoiture();
                break;
            case 4:
                supprimerVoitureDefaillante();
                break;
            case 5:
                modifierDetailsVoiture();
                break;
            case 6:
                afficherHistoriqueLocation();
                break;
            case 7:
                retournerVoiture();
                break;
            case 8:
                afficherStatistiques();
                break;
            case 9:
                printf("Fermeture de l'application E-Cars. Au revoir !\n");
                break;
            default:
                printf("Choix invalide. Veuillez réessayer.\n");
        }
    } while (choix != 9);
    return 0;
}
void afficherMenu() {
    printf("\n===== Application E-Cars =====\n");
    printf("1. Liste des Voitures Disponibles\n");
    printf("2. Louer une Voiture\n");
    printf("3. Afficher la Description d'une Voiture\n");
    printf("4. Supprimer une Voiture Défaillante\n");
    printf("5. Modifier les Détails d'une Voiture\n");
    printf("6. Afficher l'Historique des Locations\n");
    printf("7. Retourner une Voiture\n");
    printf("8. Statistiques de Location\n");
    printf("9. Quitter\n");

    int choix;
    printf("Entrez votre choix : ");
    scanf("%d", &choix);

    printf("Veuillez attendre s.v.p ");
    for (int i = 0; i < 3; ++i) {
        printf(".");
        fflush(stdout);
        sleep(1);
    }

    switch (choix) {
        case 1:
            listerVoituresDisponibles();
            break;
        case 2:
            louerVoiture();
            break;
        case 3:
            afficherDescriptionVoiture();
            break;
        case 4:
            supprimerVoitureDefaillante();
            break;
        case 5:
            modifierDetailsVoiture();
            break;
        case 6:
            afficherHistoriqueLocation();
            break;
        case 7:
            retournerVoiture();
            break;
        case 8:
            afficherStatistiques();
            break;
        case 9:
            printf("Fermeture de l'application E-Cars. Au revoir !\n");
            break;
        default:
            printf("Choix invalide. Veuillez réessayer.\n");
    }
}
void listerVoituresDisponibles() {
    int choix;
    printf("\n===== Menu Liste des Voitures Disponibles =====\n");
    printf("1. Afficher toutes les Voitures Disponibles\n");
    printf("2. Rechercher une Voiture par la première lettre du nom\n");
    printf("Entrez votre choix : ");
    scanf("%d", &choix);
    switch (choix) {
        case 1:
            printf("\n===== Voitures Disponibles =====\n");
            for (int i = 0; i < numCars; i++) {
                if (strcmp(cars[i].status, "Disponible") == 0) {
                    printf("ID de la Voiture : %d, Marque : %s, Modèle : %s\n", cars[i].id, cars[i].brand, cars[i].model);
                }
            }
            break;
        case 2:
            listerVoituresDisponiblesParLettre();
            break;
        default:
            printf("Choix invalide. Retour au menu principal.\n");
    }
}
void listerVoituresDisponiblesParLettre() {
    char lettre;
    printf("Entrez la première lettre du nom de la voiture : ");
    scanf(" %c", &lettre);
    printf("\n===== Voitures Disponibles commençant par '%c' =====\n", toupper(lettre));
    for (int i = 0; i < numCars; i++) {
        if (toupper(cars[i].brand[0]) == toupper(lettre) && strcmp(cars[i].status, "Disponible") == 0) {
            printf("ID de la Voiture : %d, Marque : %s, Modèle : %s\n", cars[i].id, cars[i].brand, cars[i].model);
        }
    }
}
void louerVoiture() {
    int idVoiture;
    printf("Entrez l'ID de la Voiture à louer : ");
    scanf("%d", &idVoiture);

    if (idVoiture >= 1 && idVoiture <= numCars && strcmp(cars[idVoiture - 1].status, "Disponible") == 0) {
        printf("Entrez la date de location (AAAA-MM-JJ) : ");
        scanf("%s", history[numRentals].rentDate);

        printf("Entrez votre adresse e-mail : ");
        scanf("%s", history[numRentals].email);

        printf("Entrez votre numéro de téléphone : ");
        scanf("%s", history[numRentals].phoneNumber);

        printf("Entrez votre nom complet (sans espace entre le nom et le prénom) : ");
        scanf("%s", history[numRentals].fullName);

        printf("Choisissez la méthode de paiement (Cash / Carte) : ");
        scanf("%s", history[numRentals].paymentMethod);
        if (strcmp(history[numRentals].paymentMethod, "Carte") == 0) {
            printf("Entrez le numéro de votre carte bancaire : ");
            scanf("%s", history[numRentals].idCardNumber);
        }

        strcpy(cars[idVoiture - 1].status, "Louée");
        history[numRentals].carId = idVoiture;
        numRentals++;

        printf("Voiture louée avec succès !\n");
    } else {
        printf("ID de la Voiture invalide ou la voiture n'est pas disponible à la location.\n");
    }
    ajouterHistorique(idVoiture, history[numRentals].rentDate, "", history[numRentals].email, history[numRentals].phoneNumber, history[numRentals].fullName, history[numRentals].idCardNumber, history[numRentals].paymentMethod, 0);
}
void recueillirAvis(int idVoiture) {
  int rating;
    printf("Entrez votre évaluation pour la voiture (1: Très mauvaise, 2: Mauvaise, 3: Médiocre, 4: Bien, 5: Très bien) : ");
    scanf("%d", &rating);
    if (rating >= 1 && rating <= 5) {
        history[idVoiture - 1].rating = rating;
        printf("Merci pour votre évaluation !\n");
    } else {
        printf("Évaluation invalide.\n");
    }
}
void afficherDescriptionVoiture() {
    int idVoiture;
    printf("Entrez l'ID de la Voiture : ");
    scanf("%d", &idVoiture);
    if (idVoiture >= 1 && idVoiture <= numCars) {
        printf("ID de la Voiture : %d, Marque : %s, Modèle : %s, Statut : %s\n",
               cars[idVoiture - 1].id, cars[idVoiture - 1].brand, cars[idVoiture - 1].model, cars[idVoiture - 1].status);
    } else {
        printf("ID de la Voiture invalide.\n");
    }
}
void supprimerVoitureDefaillante() {
   int idVoiture;
    printf("Entrez l'ID de la Voiture à supprimer : ");
    scanf("%d", &idVoiture);

    if (idVoiture >= 1 && idVoiture <= numCars) {
        for (int i = idVoiture - 1; i < numCars - 1; i++) {
            cars[i] = cars[i + 1];
        }
        numCars--;
        printf("Voiture supprimée avec succès !\n");
    } else {
        printf("ID de la Voiture invalide.\n");
    }
}
void modifierDetailsVoiture() {
    int idVoiture;
    printf("Entrez l'ID de la Voiture à modifier : ");
    scanf("%d", &idVoiture);
    if (idVoiture >= 1 && idVoiture <= numCars) {
        printf("Entrez la nouvelle marque : ");
        scanf("%s", cars[idVoiture - 1].brand);

        printf("Entrez le nouveau modèle : ");
        scanf("%s", cars[idVoiture - 1].model);

        printf("Détails de la Voiture modifiés avec succès !\n");
    } else {
        printf("ID de la Voiture invalide.\n");
    }
}
void afficherHistoriqueLocation() {
    printf("\n===== Historique des Locations =====\n");
    for (int i = 0; i < numRentals; i++) {
        printf("ID de la Voiture : %d, Date de Location : %s, Date de Retour : %s\n",
               history[i].carId, history[i].rentDate, history[i].returnDate);
        printf("Utilisateur : %s, Email : %s, Téléphone : %s\n",
               history[i].fullName, history[i].email, history[i].phoneNumber);
        printf("Méthode de paiement : %s", history[i].paymentMethod);
        if (strcmp(history[i].paymentMethod, "Carte") == 0) {
            printf(", Numéro de Carte Bancaire : %s", history[i].idCardNumber);
        }

        printf(", Évaluation : %d\n", history[i].rating);
        printf("=======================================\n");
    }
}
void retournerVoiture() {
    int idVoiture;
    printf("Entrez l'ID de la Voiture à retourner : ");
    scanf("%d", &idVoiture);

    if (idVoiture >= 1 && idVoiture <= numCars && strcmp(cars[idVoiture - 1].status, "Louée") == 0) {
        printf("Entrez la date de retour (AAAA-MM-JJ) : ");
       int rentalIndex = -1;
for (int i = 0; i < numRentals; i++) {
    if (history[i].carId == idVoiture) {
        rentalIndex = i;
        break;
    }
}
if (rentalIndex != -1) {
    scanf("%s", history[rentalIndex].returnDate);
    recueillirAvis(rentalIndex);
} else {
    printf("Aucun enregistrement de location trouvé pour la voiture spécifiée.\n");
}
        strcpy(cars[idVoiture - 1].status, "Disponible");
        printf("Voiture retournée avec succès !\n");
    } else {
        printf("ID de la Voiture invalide ou la voiture n'est pas actuellement louée.\n");
    }
    recueillirAvis(numRentals - 1);
}
void afficherStatistiques() {
    printf("\n===== Statistiques de Location =====\n");
    for (int i = 0; i < numCars; i++) {
        int timesRented = 0;
        for (int j = 0; j < numRentals; j++) {
            if (history[j].carId == cars[i].id) {
                timesRented++;
            }
        }
        double percentage = (timesRented / (double)numRentals) * 100.0;
        printf("ID de la Voiture : %d, Marque : %s, Modèle : %s, Pourcentage de Location : %.2f%%\n",
               cars[i].id, cars[i].brand, cars[i].model, percentage);
    }
}
