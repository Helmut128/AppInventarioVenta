Avances del proyecto (no me corran del grupo XD )



<div class="body">
  <div class="login">
    <mat-spinner *ngIf="loading" class="spinner" diameter="50"></mat-spinner>
    <form *ngIf="!loading" [formGroup]="form" (ngSubmit)="ingresar()">
      <img src="./assets/img/usuario.png" alt="" width="50%" />
      <h1>login</h1>
      <mat-form-field class="ancho" appearance="fill">
        <mat-label>Usuario</mat-label>
        <input
          type="text"
          matInput
          autocomplete="off"
          formControlName="usuario"
        />
      </mat-form-field>
      <mat-form-field class="ancho" appearance="fill">
        <mat-label>Contraseña</mat-label>
        <input
          type="password"
          matInput
          autocomplete="off"
          formControlName="password"
        />
      </mat-form-field>
      <br />
      <button
        type="submit"
        class="ancho button"
        mat-raised-button
        color="Primary"
        [disabled]="form.invalid"
      >
        Ingresar
      </button>
    </form>
  </div>
</div>

