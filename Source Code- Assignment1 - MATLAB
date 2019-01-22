DateVector = datevec(Encounter_date);
for j = 2:5674
    DateVector(j,1) = DateVector(j,1) + 1900;
    YearEncountered(j-1,1) = DateVector(j,1);
end


a = 1;
b = 1;
c = 1;
d = 1;
Genderstr = char(Gender);
for j = 1:5674
    if Depression(j,1) == 1
        if Genderstr(j,1) == 'M'
            DepressionMListYears(a,1) = YearEncountered(j,1);
            a = a +1;
        else
            DepressionFListYears(a,1) = YearEncountered(j,1);
            a = a +1;
        end 
    elseif Anxiety(j,1) == 1
        if Genderstr(j,1) == 'M'
            AnxietyMListYears(b,1) = YearEncountered(j,1);
            b = b +1;
        else
            AnxietyFListYears(b,1) = YearEncountered(j,1);
            b = b +1;
        end 
    elseif Headache(j,1) ==1
        if Genderstr(j,1) == 'M'
            HeadacheMListYears(c,1) = YearEncountered(j,1);
            c = c +1;
        else
            HeadacheFListYears(c,1) = YearEncountered(j,1);
            c = c +1;
        end 
    elseif Sleep(j,1) ==1
        if Genderstr(j,1) == 'M'
            SleepMListYears(d,1) = YearEncountered(j,1);
            d = d +1;
        else
            SleepFListYears(d,1) = YearEncountered(j,1);
            d = d +1;
        end 
    end    
    
end

count = 2006;
for i = 1:10
    Encounter_Year(i,1) = count;
    count = count + 1;
end
DepressionMCounts=arrayfun(@(x) sum(DepressionMListYears==x),unqValue);
DepressionFCounts=arrayfun(@(x) sum(DepressionFListYears==x),unqValue);
AnxietyMCounts=arrayfun(@(x) sum(AnxietyMListYears==x),unqValue);
AnxietyFCounts=arrayfun(@(x) sum(AnxietyFListYears==x),unqValue);
HeadacheMCounts=arrayfun(@(x) sum(HeadacheMListYears==x),unqValue);
HeadacheFCounts=arrayfun(@(x) sum(HeadacheFListYears==x),unqValue);
SleepMCounts=arrayfun(@(x) sum(SleepMListYears==x),unqValue);
SleepFCounts=arrayfun(@(x) sum(SleepFListYears==x),unqValue);
 
subplot(4,1,1);
plot(Encounter_Year, AnxietyMCounts);
hold on 
plot(Encounter_Year, AnxietyFCounts);
hold off
title('Anxiety Encounters by Year by Gender');
xlabel('Year of Encounter Date')
ylabel('Count')
legend({'y = Female','y = Male'},'Location','southwest')


subplot(4,1,2);
plot(Encounter_Year, DepressionMCounts);
hold on 
plot(Encounter_Year, DepressionFCounts);
hold off
title('Depression Encounters by Year by Gender');
xlabel('Year of Encounter Date')
ylabel('Count')

subplot(4,1,3);
plot(Encounter_Year, SleepMCounts);
hold on
plot(Encounter_Year, SleepFCounts);
hold off
title('Sleep Encounters by Year by Gender');
xlabel('Year of Encounter Date')
ylabel('Count')

subplot(4,1,4);
plot(Encounter_Year, HeadacheMCounts);
hold on
plot(Encounter_Year, HeadacheFCounts);
hold off
title('Headache Encounters by Year by Gender');
xlabel('Year of Encounter Date')
ylabel('Count')
