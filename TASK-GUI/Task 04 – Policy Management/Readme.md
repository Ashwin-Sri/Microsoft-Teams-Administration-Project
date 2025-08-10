# Task 04 – Policy Management

This task outlines how to create and assign custom messaging, meeting, and app permission policies in Microsoft Teams. All configurations are performed via the Teams Admin Center.

---

## Objective

- Create messaging policies to control chat, file sharing, and media usage  
- Create meeting policies to manage recording, chat, and join behavior  
- Create app permission policies to allow or block Microsoft, third-party, and tenant apps  

---

## Task List

| Step | Task Description |
|------|------------------|
| 1 | Create a custom Messaging Policy |
| 2 | Create a custom Meeting Policy |
| 3 | Assign policies to users via Teams Admin Center |
| 4 | Validate policy assignment and behavior |

---

## Steps

### Step 1 – Create a Custom Messaging Policy

1. Go to [Teams Admin Center](https://admin.teams.microsoft.com)  
2. Navigate to **Settings & policies > Custom policies for users and groups > Messaging**
 
   <img width="1662" height="686" alt="image" src="https://github.com/user-attachments/assets/718f1566-c686-4e7d-a26f-03606fc7389b" />

4. Click **Add**  
5. Enter a name (e.g., `CustomMessagingPolicy`)  
6. Configure settings:
   - **Chat**: On  
   - **Giphy**: Off  
   - **Stickers**: Off  
   - **URL previews**: On  
   - **Read receipts**: User controlled  
7. Click **Save**

   <img width="1602" height="867" alt="image" src="https://github.com/user-attachments/assets/d7a5fcf4-1cdf-4530-aaec-a4cf445b32bb" />

---

### Step 2 – Create a Custom Meeting Policy

1. In Teams Admin Center, go to **Meetings > Meeting policies**  
2. Click **Add**  
3. Enter a name (e.g., `CustomMeetingPolicy`)

   <img width="1546" height="852" alt="image" src="https://github.com/user-attachments/assets/f339404a-3f9b-418d-8705-fa166ef0f72e" />

5. Configure settings:
   - **Allow recording**: Off  
   - **Allow transcription**: Off  
   - **Allow chat in meetings**: Enabled  
6. Click **Save**

<img width="1337" height="812" alt="image" src="https://github.com/user-attachments/assets/3afa5d02-9698-4ffb-9ec0-c80cecc4efba" />

---

### Step 3 – Assign Policies to Users

1. Go to **Users** in Teams Admin Center  
2. Select a user  
3. Under **Policies**, click **Edit**

   <img width="1048" height="823" alt="image" src="https://github.com/user-attachments/assets/65fdcac6-a573-44dd-8787-8bb720a671b8" />

5. Assign:
   - **Messaging policy**: `CustomMessagingPolicy`  
   - **Meeting policy**: `CustomMeetingPolicy`  
6. Click **Apply**

<img width="1903" height="848" alt="image" src="https://github.com/user-attachments/assets/8ac135fd-092d-4ae5-aa07-10067cbba172" />

---

### Step 4 – Validate Policy Assignment

1. Return to **Users**  
2. Select the same user  
3. Confirm assigned policies reflect the custom ones  
4. Optionally, sign in as the user and verify Teams behavior matches policy settings

<img width="878" height="812" alt="image" src="https://github.com/user-attachments/assets/8617bf3a-8592-4501-82dd-d84bcb2c52de" />

---

## Outcome

- Messaging, meeting, and app permission policies are created and assigned  
- User experience is tailored to organizational standards  
- All configurations are validated via the Teams Admin Center

  ---
